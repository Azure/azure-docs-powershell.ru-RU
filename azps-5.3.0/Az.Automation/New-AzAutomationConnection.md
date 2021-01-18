---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 95103160-8101-4C43-8DAA-0BD75DFF3150
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/new-azautomationconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationConnection.md
ms.openlocfilehash: f9a332aaf50f60940391a52549d6f5549c77198b
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98509997"
---
# <span data-ttu-id="6b679-101">New-AzAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="6b679-101">New-AzAutomationConnection</span></span>

## <span data-ttu-id="6b679-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6b679-102">SYNOPSIS</span></span>
<span data-ttu-id="6b679-103">Создает соединение автоматизации.</span><span class="sxs-lookup"><span data-stu-id="6b679-103">Creates an Automation connection.</span></span>

## <span data-ttu-id="6b679-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="6b679-104">SYNTAX</span></span>

```
New-AzAutomationConnection [-Name] <String> [-ConnectionTypeName] <String>
 [-ConnectionFieldValues] <IDictionary> [-Description <String>] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6b679-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="6b679-105">DESCRIPTION</span></span>
<span data-ttu-id="6b679-106">Для создания соединения в автоматизации Azure создается **cmdlet New-AzAutomationConnection.**</span><span class="sxs-lookup"><span data-stu-id="6b679-106">The **New-AzAutomationConnection** cmdlet creates a connection in Azure Automation.</span></span>

## <span data-ttu-id="6b679-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="6b679-107">EXAMPLES</span></span>

### <span data-ttu-id="6b679-108">Пример 1. Создание подключения для ConnectionTypeName=Azure</span><span class="sxs-lookup"><span data-stu-id="6b679-108">Example 1: Create a connection for ConnectionTypeName=Azure</span></span>
```
PS C:\> $FieldValues = @{"AutomationCertificateName"="ContosoCertificate";"SubscriptionID"="81b59010-dc55-45b7-89cd-5ca26db62472"}
PS C:\> New-AzAutomationConnection -Name "Connection12" -ConnectionTypeName Azure -ConnectionFieldValues $FieldValues -ResourceGroupName "ResourceGroup01" -AutomationAccountName "AutomationAccount01"
```

<span data-ttu-id="6b679-109">Первая команда назначает таблицу значений полей переменной $FieldValue.</span><span class="sxs-lookup"><span data-stu-id="6b679-109">The first command assigns a hash table of field values to the $FieldValue variable.</span></span>
<span data-ttu-id="6b679-110">Вторая команда создает подключение Azure с именем Connection12 в учетной записи автоматизации с именем AutomationAccount01.</span><span class="sxs-lookup"><span data-stu-id="6b679-110">The second command creates an Azure connection named Connection12 in the Automation account named AutomationAccount01.</span></span>
<span data-ttu-id="6b679-111">Для этой команды используются значения поля подключения в $FieldValues.</span><span class="sxs-lookup"><span data-stu-id="6b679-111">The command uses the connection field values in $FieldValues.</span></span>

### <span data-ttu-id="6b679-112">Пример 2. Создание подключения для ConnectionTypeName=AzureServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="6b679-112">Example 2: Create a connection for ConnectionTypeName=AzureServicePrincipal</span></span>
```
PS C:\> $Thumbprint = "0SZTNJ34TCCMUJ5MJZGR8XQD3S0RVHJBA33Z8ZXV"
PS C:\> $TenantId = "4cd76576-b611-43d0-8f2b-adcb139531bf"
PS C:\> $ApplicationId = "3794a65a-e4e4-493d-ac1d-f04308d712dd"
PS C:\> $SubscriptionId = "81b59010-dc55-45b7-89cd-5ca26db62472"
PS C:\> $RunAsAccountConnectionFieldValues = @{"ApplicationId" = $ApplicationId; "TenantId" = $TenantId; "CertificateThumbprint" = $Thumbprint; "SubscriptionId" = $SubscriptionId}
PS C:\> New-AzAutomationConnection -Name "Connection13" -ConnectionTypeName AzureServicePrincipal -ConnectionFieldValues $RunAsAccountConnectionFieldValues -ResourceGroupName "ResourceGroup01" -AutomationAccountName "AutomationAccount01"
```

<span data-ttu-id="6b679-113">Команда создает подключение Azure с именем Connection13 в учетной записи автоматизации с именем AutomationAccount01, используя $RunAsAccountConnectionFieldValues и ConnectionTypeName=AzureServicePrincipal.</span><span class="sxs-lookup"><span data-stu-id="6b679-113">The command creates an Azure connection named Connection13 in the Automation account named AutomationAccount01 using $RunAsAccountConnectionFieldValues and ConnectionTypeName=AzureServicePrincipal.</span></span>
<span data-ttu-id="6b679-114">Это имя ConnectionTypeName=AzureServicePrincipal в основном используется для azure Run As Account.</span><span class="sxs-lookup"><span data-stu-id="6b679-114">This ConnectionTypeName=AzureServicePrincipal is mainly used for Azure Run As Account.</span></span>

### <span data-ttu-id="6b679-115">Пример 3. Создание подключения для ConnectionTypeName=AzureClassicCertificate</span><span class="sxs-lookup"><span data-stu-id="6b679-115">Example 3: Create a connection for ConnectionTypeName=AzureClassicCertificate</span></span>
```
PS C:\> $SubscriptionName = "MyTestSubscription"
PS C:\> $SubscriptionId = "81b59010-dc55-45b7-89cd-5ca26db62472"
PS C:\> $ClassicRunAsAccountCertifcateAssetName = "AzureClassicRunAsCertificate"
PS C:\> $ClassicRunAsAccountConnectionFieldValues = @{"SubscriptionName" = $SubscriptionName; "SubscriptionId" = $SubscriptionId; "CertificateAssetName" = $ClassicRunAsAccountCertifcateAssetName}
PS C:\> New-AzAutomationConnection -Name "Connection14" -ConnectionTypeName AzureClassicCertificate  -ConnectionFieldValues $ClassicRunAsAccountConnectionFieldValues -ResourceGroupName "ResourceGroup01" -AutomationAccountName "AutomationAccount01"
```

<span data-ttu-id="6b679-116">Команда создает подключение Azure с именем Connection14 в учетной записи автоматизации AutomationAccount01, используя $ClassicRunAsAccountConnectionFieldValues и ConnectionTypeName=AzureClassicCertificate.</span><span class="sxs-lookup"><span data-stu-id="6b679-116">The command creates an Azure connection named Connection14 in the Automation account named AutomationAccount01 using $ClassicRunAsAccountConnectionFieldValues and ConnectionTypeName=AzureClassicCertificate.</span></span>
<span data-ttu-id="6b679-117">Это connectionTypeName=AzureClassicCertificate в основном используется для azure Classic Run As Account.</span><span class="sxs-lookup"><span data-stu-id="6b679-117">This ConnectionTypeName=AzureClassicCertificate is mainly used for Azure Classic Run As Account.</span></span>

## <span data-ttu-id="6b679-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6b679-118">PARAMETERS</span></span>

### <span data-ttu-id="6b679-119">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="6b679-119">-AutomationAccountName</span></span>
<span data-ttu-id="6b679-120">Указывает имя учетной записи автоматизации, для которой этот cmdlet создает подключение.</span><span class="sxs-lookup"><span data-stu-id="6b679-120">Specifies the name of the Automation account for which this cmdlet creates a connection.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6b679-121">-ConnectionFieldValues</span><span class="sxs-lookup"><span data-stu-id="6b679-121">-ConnectionFieldValues</span></span>
<span data-ttu-id="6b679-122">Определяет таблицу с ключами и значениями.</span><span class="sxs-lookup"><span data-stu-id="6b679-122">Specifies a hash table that contains key/value pairs.</span></span>
<span data-ttu-id="6b679-123">Ключи представляют поля подключения для указанного типа подключения.</span><span class="sxs-lookup"><span data-stu-id="6b679-123">The keys represent the connection fields for the specified connection type.</span></span>
<span data-ttu-id="6b679-124">Значения представляют конкретные значения каждого поля подключения для экземпляра подключения.</span><span class="sxs-lookup"><span data-stu-id="6b679-124">The values represent the specific values of each connection field for the connection instance.</span></span>

```yaml
Type: System.Collections.IDictionary
Parameter Sets: (All)
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6b679-125">-ConnectionTypeName</span><span class="sxs-lookup"><span data-stu-id="6b679-125">-ConnectionTypeName</span></span>
<span data-ttu-id="6b679-126">Указывает имя типа подключения.</span><span class="sxs-lookup"><span data-stu-id="6b679-126">Specifies the name of the connection type.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6b679-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6b679-127">-DefaultProfile</span></span>
<span data-ttu-id="6b679-128">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="6b679-128">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6b679-129">-Description</span><span class="sxs-lookup"><span data-stu-id="6b679-129">-Description</span></span>
<span data-ttu-id="6b679-130">Описание подключения.</span><span class="sxs-lookup"><span data-stu-id="6b679-130">Specifies a description for the connection.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6b679-131">-Name</span><span class="sxs-lookup"><span data-stu-id="6b679-131">-Name</span></span>
<span data-ttu-id="6b679-132">Указывает имя подключения.</span><span class="sxs-lookup"><span data-stu-id="6b679-132">Specifies a name for the connection.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6b679-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6b679-133">-ResourceGroupName</span></span>
<span data-ttu-id="6b679-134">Указывает имя группы ресурсов, для которой этот cmdlet создает подключение.</span><span class="sxs-lookup"><span data-stu-id="6b679-134">Specifies the name of the resource group for which this cmdlet creates a connection.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6b679-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6b679-135">CommonParameters</span></span>
<span data-ttu-id="6b679-136">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6b679-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6b679-137">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6b679-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6b679-138">INPUTS</span><span class="sxs-lookup"><span data-stu-id="6b679-138">INPUTS</span></span>

### <span data-ttu-id="6b679-139">System.String</span><span class="sxs-lookup"><span data-stu-id="6b679-139">System.String</span></span>

### <span data-ttu-id="6b679-140">System.Collections.IDictionary</span><span class="sxs-lookup"><span data-stu-id="6b679-140">System.Collections.IDictionary</span></span>

## <span data-ttu-id="6b679-141">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="6b679-141">OUTPUTS</span></span>

### <span data-ttu-id="6b679-142">Microsoft.Azure.Commands.Automation.Model.Connection</span><span class="sxs-lookup"><span data-stu-id="6b679-142">Microsoft.Azure.Commands.Automation.Model.Connection</span></span>

## <span data-ttu-id="6b679-143">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="6b679-143">NOTES</span></span>

## <span data-ttu-id="6b679-144">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="6b679-144">RELATED LINKS</span></span>

[<span data-ttu-id="6b679-145">Get-AzAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="6b679-145">Get-AzAutomationConnection</span></span>](./Get-AzAutomationConnection.md)

[<span data-ttu-id="6b679-146">Remove-AzAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="6b679-146">Remove-AzAutomationConnection</span></span>](./Remove-AzAutomationConnection.md)


