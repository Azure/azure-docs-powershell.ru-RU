---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 95103160-8101-4C43-8DAA-0BD75DFF3150
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/New-AzureRMAutomationConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/New-AzureRMAutomationConnection.md
ms.openlocfilehash: 2964102dbb3f12b797d3d551f7bd4097ca8836a5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93565686"
---
# <span data-ttu-id="6f7fa-101">New-AzureRmAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="6f7fa-101">New-AzureRmAutomationConnection</span></span>

## <span data-ttu-id="6f7fa-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="6f7fa-102">SYNOPSIS</span></span>
<span data-ttu-id="6f7fa-103">Создает подключение автоматизации.</span><span class="sxs-lookup"><span data-stu-id="6f7fa-103">Creates an Automation connection.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6f7fa-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="6f7fa-104">SYNTAX</span></span>

```
New-AzureRmAutomationConnection [-Name] <String> [-ConnectionTypeName] <String>
 [-ConnectionFieldValues] <IDictionary> [-Description <String>] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6f7fa-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="6f7fa-105">DESCRIPTION</span></span>
<span data-ttu-id="6f7fa-106">Командлет **New-AzureRmAutomationConnection** создает подключение в службе автоматизации Azure.</span><span class="sxs-lookup"><span data-stu-id="6f7fa-106">The **New-AzureRmAutomationConnection** cmdlet creates a connection in Azure Automation.</span></span>

## <span data-ttu-id="6f7fa-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="6f7fa-107">EXAMPLES</span></span>

### <span data-ttu-id="6f7fa-108">Пример 1: создание подключения</span><span class="sxs-lookup"><span data-stu-id="6f7fa-108">Example 1: Create a connection</span></span>
```
PS C:\>$FieldValues = @{"AutomationCertificateName"="ContosoCertificate";"SubscriptionID"="81b59010-dc55-45b7-89cd-5ca26db62472"}
PS C:\> New-AzureRmAutomationConnection -Name "Connection12" -ConnectionTypeName Azure -ConnectionFieldValues $FieldValues -ResourceGroupName "ResourceGroup01" -AutomationAccountName "AutomationAccount01"
```

<span data-ttu-id="6f7fa-109">Первая команда назначает хэш-таблицу значений полей переменной $FieldValue.</span><span class="sxs-lookup"><span data-stu-id="6f7fa-109">The first command assigns a hash table of field values to the $FieldValue variable.</span></span>

<span data-ttu-id="6f7fa-110">Вторая команда создает подключение Azure с именем Connection12 в учетной записи автоматизации с именем AutomationAccount01.</span><span class="sxs-lookup"><span data-stu-id="6f7fa-110">The second command creates an Azure connection named Connection12 in the Automation account named AutomationAccount01.</span></span>
<span data-ttu-id="6f7fa-111">Команда использует значения полей подключения в $FieldValues.</span><span class="sxs-lookup"><span data-stu-id="6f7fa-111">The command uses the connection field values in $FieldValues.</span></span>

## <span data-ttu-id="6f7fa-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="6f7fa-112">PARAMETERS</span></span>

### <span data-ttu-id="6f7fa-113">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="6f7fa-113">-AutomationAccountName</span></span>
<span data-ttu-id="6f7fa-114">Указывает имя учетной записи автоматизации, для которой этот командлет создает подключение.</span><span class="sxs-lookup"><span data-stu-id="6f7fa-114">Specifies the name of the Automation account for which this cmdlet creates a connection.</span></span>

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

### <span data-ttu-id="6f7fa-115">-ConnectionFieldValues</span><span class="sxs-lookup"><span data-stu-id="6f7fa-115">-ConnectionFieldValues</span></span>
<span data-ttu-id="6f7fa-116">Указывает хэш-таблицу, которая содержит пары "ключ-значение".</span><span class="sxs-lookup"><span data-stu-id="6f7fa-116">Specifies a hash table that contains key/value pairs.</span></span>
<span data-ttu-id="6f7fa-117">Ключи представляют поля соединения для указанного типа подключения.</span><span class="sxs-lookup"><span data-stu-id="6f7fa-117">The keys represent the connection fields for the specified connection type.</span></span>
<span data-ttu-id="6f7fa-118">Значения представляют конкретные значения каждого поля соединения для экземпляра Connection.</span><span class="sxs-lookup"><span data-stu-id="6f7fa-118">The values represent the specific values of each connection field for the connection instance.</span></span>

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

### <span data-ttu-id="6f7fa-119">-ConnectionTypeName</span><span class="sxs-lookup"><span data-stu-id="6f7fa-119">-ConnectionTypeName</span></span>
<span data-ttu-id="6f7fa-120">Указывает имя типа подключения.</span><span class="sxs-lookup"><span data-stu-id="6f7fa-120">Specifies the name of the connection type.</span></span>

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

### <span data-ttu-id="6f7fa-121">-Описание</span><span class="sxs-lookup"><span data-stu-id="6f7fa-121">-Description</span></span>
<span data-ttu-id="6f7fa-122">Задает описание подключения.</span><span class="sxs-lookup"><span data-stu-id="6f7fa-122">Specifies a description for the connection.</span></span>

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

### <span data-ttu-id="6f7fa-123">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="6f7fa-123">-Name</span></span>
<span data-ttu-id="6f7fa-124">Задает имя для подключения.</span><span class="sxs-lookup"><span data-stu-id="6f7fa-124">Specifies a name for the connection.</span></span>

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

### <span data-ttu-id="6f7fa-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6f7fa-125">-ResourceGroupName</span></span>
<span data-ttu-id="6f7fa-126">Указывает имя группы ресурсов, для которой этот командлет создает подключение.</span><span class="sxs-lookup"><span data-stu-id="6f7fa-126">Specifies the name of the resource group for which this cmdlet creates a connection.</span></span>

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

### <span data-ttu-id="6f7fa-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6f7fa-127">-DefaultProfile</span></span>
<span data-ttu-id="6f7fa-128">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="6f7fa-128">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6f7fa-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6f7fa-129">CommonParameters</span></span>
<span data-ttu-id="6f7fa-130">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="6f7fa-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6f7fa-131">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6f7fa-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6f7fa-132">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="6f7fa-132">INPUTS</span></span>

## <span data-ttu-id="6f7fa-133">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="6f7fa-133">OUTPUTS</span></span>

### <span data-ttu-id="6f7fa-134">Microsoft. Azure. Commands. Automation. Model. Connection</span><span class="sxs-lookup"><span data-stu-id="6f7fa-134">Microsoft.Azure.Commands.Automation.Model.Connection</span></span>

## <span data-ttu-id="6f7fa-135">Пуск</span><span class="sxs-lookup"><span data-stu-id="6f7fa-135">NOTES</span></span>

## <span data-ttu-id="6f7fa-136">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="6f7fa-136">RELATED LINKS</span></span>

[<span data-ttu-id="6f7fa-137">Get-AzureRmAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="6f7fa-137">Get-AzureRmAutomationConnection</span></span>](./Get-AzureRMAutomationConnection.md)

[<span data-ttu-id="6f7fa-138">Remove-AzureRmAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="6f7fa-138">Remove-AzureRmAutomationConnection</span></span>](./Remove-AzureRMAutomationConnection.md)


