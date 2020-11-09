---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 95103160-8101-4C43-8DAA-0BD75DFF3150
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/new-azautomationconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationConnection.md
ms.openlocfilehash: f9a332aaf50f60940391a52549d6f5549c77198b
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94316223"
---
# <span data-ttu-id="4e70f-101">New-AzAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="4e70f-101">New-AzAutomationConnection</span></span>

## <span data-ttu-id="4e70f-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="4e70f-102">SYNOPSIS</span></span>
<span data-ttu-id="4e70f-103">Создает подключение автоматизации.</span><span class="sxs-lookup"><span data-stu-id="4e70f-103">Creates an Automation connection.</span></span>

## <span data-ttu-id="4e70f-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="4e70f-104">SYNTAX</span></span>

```
New-AzAutomationConnection [-Name] <String> [-ConnectionTypeName] <String>
 [-ConnectionFieldValues] <IDictionary> [-Description <String>] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4e70f-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="4e70f-105">DESCRIPTION</span></span>
<span data-ttu-id="4e70f-106">Командлет **New-AzAutomationConnection** создает подключение в службе автоматизации Azure.</span><span class="sxs-lookup"><span data-stu-id="4e70f-106">The **New-AzAutomationConnection** cmdlet creates a connection in Azure Automation.</span></span>

## <span data-ttu-id="4e70f-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="4e70f-107">EXAMPLES</span></span>

### <span data-ttu-id="4e70f-108">Пример 1: создание подключения для ConnectionTypeName = Azure</span><span class="sxs-lookup"><span data-stu-id="4e70f-108">Example 1: Create a connection for ConnectionTypeName=Azure</span></span>
```
PS C:\> $FieldValues = @{"AutomationCertificateName"="ContosoCertificate";"SubscriptionID"="81b59010-dc55-45b7-89cd-5ca26db62472"}
PS C:\> New-AzAutomationConnection -Name "Connection12" -ConnectionTypeName Azure -ConnectionFieldValues $FieldValues -ResourceGroupName "ResourceGroup01" -AutomationAccountName "AutomationAccount01"
```

<span data-ttu-id="4e70f-109">Первая команда назначает хэш-таблицу значений полей переменной $FieldValue.</span><span class="sxs-lookup"><span data-stu-id="4e70f-109">The first command assigns a hash table of field values to the $FieldValue variable.</span></span>
<span data-ttu-id="4e70f-110">Вторая команда создает подключение Azure с именем Connection12 в учетной записи автоматизации с именем AutomationAccount01.</span><span class="sxs-lookup"><span data-stu-id="4e70f-110">The second command creates an Azure connection named Connection12 in the Automation account named AutomationAccount01.</span></span>
<span data-ttu-id="4e70f-111">Команда использует значения полей подключения в $FieldValues.</span><span class="sxs-lookup"><span data-stu-id="4e70f-111">The command uses the connection field values in $FieldValues.</span></span>

### <span data-ttu-id="4e70f-112">Пример 2: создание подключения для ConnectionTypeName = AzureServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="4e70f-112">Example 2: Create a connection for ConnectionTypeName=AzureServicePrincipal</span></span>
```
PS C:\> $Thumbprint = "0SZTNJ34TCCMUJ5MJZGR8XQD3S0RVHJBA33Z8ZXV"
PS C:\> $TenantId = "4cd76576-b611-43d0-8f2b-adcb139531bf"
PS C:\> $ApplicationId = "3794a65a-e4e4-493d-ac1d-f04308d712dd"
PS C:\> $SubscriptionId = "81b59010-dc55-45b7-89cd-5ca26db62472"
PS C:\> $RunAsAccountConnectionFieldValues = @{"ApplicationId" = $ApplicationId; "TenantId" = $TenantId; "CertificateThumbprint" = $Thumbprint; "SubscriptionId" = $SubscriptionId}
PS C:\> New-AzAutomationConnection -Name "Connection13" -ConnectionTypeName AzureServicePrincipal -ConnectionFieldValues $RunAsAccountConnectionFieldValues -ResourceGroupName "ResourceGroup01" -AutomationAccountName "AutomationAccount01"
```

<span data-ttu-id="4e70f-113">Команда создает подключение Azure с именем Connection13 в учетной записи автоматизации с именем AutomationAccount01 с помощью $RunAsAccountConnectionFieldValues и ConnectionTypeName = AzureServicePrincipal.</span><span class="sxs-lookup"><span data-stu-id="4e70f-113">The command creates an Azure connection named Connection13 in the Automation account named AutomationAccount01 using $RunAsAccountConnectionFieldValues and ConnectionTypeName=AzureServicePrincipal.</span></span>
<span data-ttu-id="4e70f-114">Этот ConnectionTypeName = AzureServicePrincipal преимущественно используется для учетной записи запуска от имени Azure.</span><span class="sxs-lookup"><span data-stu-id="4e70f-114">This ConnectionTypeName=AzureServicePrincipal is mainly used for Azure Run As Account.</span></span>

### <span data-ttu-id="4e70f-115">Пример 3: создание подключения для ConnectionTypeName = AzureClassicCertificate</span><span class="sxs-lookup"><span data-stu-id="4e70f-115">Example 3: Create a connection for ConnectionTypeName=AzureClassicCertificate</span></span>
```
PS C:\> $SubscriptionName = "MyTestSubscription"
PS C:\> $SubscriptionId = "81b59010-dc55-45b7-89cd-5ca26db62472"
PS C:\> $ClassicRunAsAccountCertifcateAssetName = "AzureClassicRunAsCertificate"
PS C:\> $ClassicRunAsAccountConnectionFieldValues = @{"SubscriptionName" = $SubscriptionName; "SubscriptionId" = $SubscriptionId; "CertificateAssetName" = $ClassicRunAsAccountCertifcateAssetName}
PS C:\> New-AzAutomationConnection -Name "Connection14" -ConnectionTypeName AzureClassicCertificate  -ConnectionFieldValues $ClassicRunAsAccountConnectionFieldValues -ResourceGroupName "ResourceGroup01" -AutomationAccountName "AutomationAccount01"
```

<span data-ttu-id="4e70f-116">Команда создает подключение Azure с именем Connection14 в учетной записи автоматизации с именем AutomationAccount01 с помощью $ClassicRunAsAccountConnectionFieldValues и ConnectionTypeName = AzureClassicCertificate.</span><span class="sxs-lookup"><span data-stu-id="4e70f-116">The command creates an Azure connection named Connection14 in the Automation account named AutomationAccount01 using $ClassicRunAsAccountConnectionFieldValues and ConnectionTypeName=AzureClassicCertificate.</span></span>
<span data-ttu-id="4e70f-117">Этот ConnectionTypeName = AzureClassicCertificate преимущественно используется для классической учетной записи запуска от имени Azure.</span><span class="sxs-lookup"><span data-stu-id="4e70f-117">This ConnectionTypeName=AzureClassicCertificate is mainly used for Azure Classic Run As Account.</span></span>

## <span data-ttu-id="4e70f-118">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="4e70f-118">PARAMETERS</span></span>

### <span data-ttu-id="4e70f-119">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="4e70f-119">-AutomationAccountName</span></span>
<span data-ttu-id="4e70f-120">Указывает имя учетной записи автоматизации, для которой этот командлет создает подключение.</span><span class="sxs-lookup"><span data-stu-id="4e70f-120">Specifies the name of the Automation account for which this cmdlet creates a connection.</span></span>

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

### <span data-ttu-id="4e70f-121">-ConnectionFieldValues</span><span class="sxs-lookup"><span data-stu-id="4e70f-121">-ConnectionFieldValues</span></span>
<span data-ttu-id="4e70f-122">Указывает хэш-таблицу, которая содержит пары "ключ-значение".</span><span class="sxs-lookup"><span data-stu-id="4e70f-122">Specifies a hash table that contains key/value pairs.</span></span>
<span data-ttu-id="4e70f-123">Ключи представляют поля соединения для указанного типа подключения.</span><span class="sxs-lookup"><span data-stu-id="4e70f-123">The keys represent the connection fields for the specified connection type.</span></span>
<span data-ttu-id="4e70f-124">Значения представляют конкретные значения каждого поля соединения для экземпляра Connection.</span><span class="sxs-lookup"><span data-stu-id="4e70f-124">The values represent the specific values of each connection field for the connection instance.</span></span>

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

### <span data-ttu-id="4e70f-125">-ConnectionTypeName</span><span class="sxs-lookup"><span data-stu-id="4e70f-125">-ConnectionTypeName</span></span>
<span data-ttu-id="4e70f-126">Указывает имя типа подключения.</span><span class="sxs-lookup"><span data-stu-id="4e70f-126">Specifies the name of the connection type.</span></span>

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

### <span data-ttu-id="4e70f-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4e70f-127">-DefaultProfile</span></span>
<span data-ttu-id="4e70f-128">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="4e70f-128">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4e70f-129">-Описание</span><span class="sxs-lookup"><span data-stu-id="4e70f-129">-Description</span></span>
<span data-ttu-id="4e70f-130">Задает описание подключения.</span><span class="sxs-lookup"><span data-stu-id="4e70f-130">Specifies a description for the connection.</span></span>

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

### <span data-ttu-id="4e70f-131">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="4e70f-131">-Name</span></span>
<span data-ttu-id="4e70f-132">Задает имя для подключения.</span><span class="sxs-lookup"><span data-stu-id="4e70f-132">Specifies a name for the connection.</span></span>

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

### <span data-ttu-id="4e70f-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4e70f-133">-ResourceGroupName</span></span>
<span data-ttu-id="4e70f-134">Указывает имя группы ресурсов, для которой этот командлет создает подключение.</span><span class="sxs-lookup"><span data-stu-id="4e70f-134">Specifies the name of the resource group for which this cmdlet creates a connection.</span></span>

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

### <span data-ttu-id="4e70f-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4e70f-135">CommonParameters</span></span>
<span data-ttu-id="4e70f-136">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="4e70f-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4e70f-137">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4e70f-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4e70f-138">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="4e70f-138">INPUTS</span></span>

### <span data-ttu-id="4e70f-139">System. String</span><span class="sxs-lookup"><span data-stu-id="4e70f-139">System.String</span></span>

### <span data-ttu-id="4e70f-140">System. Collections. IDictionary</span><span class="sxs-lookup"><span data-stu-id="4e70f-140">System.Collections.IDictionary</span></span>

## <span data-ttu-id="4e70f-141">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="4e70f-141">OUTPUTS</span></span>

### <span data-ttu-id="4e70f-142">Microsoft. Azure. Commands. Automation. Model. Connection</span><span class="sxs-lookup"><span data-stu-id="4e70f-142">Microsoft.Azure.Commands.Automation.Model.Connection</span></span>

## <span data-ttu-id="4e70f-143">Пуск</span><span class="sxs-lookup"><span data-stu-id="4e70f-143">NOTES</span></span>

## <span data-ttu-id="4e70f-144">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="4e70f-144">RELATED LINKS</span></span>

[<span data-ttu-id="4e70f-145">Get-AzAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="4e70f-145">Get-AzAutomationConnection</span></span>](./Get-AzAutomationConnection.md)

[<span data-ttu-id="4e70f-146">Remove-AzAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="4e70f-146">Remove-AzAutomationConnection</span></span>](./Remove-AzAutomationConnection.md)


