---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 95103160-8101-4C43-8DAA-0BD75DFF3150
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/new-azautomationconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationConnection.md
ms.openlocfilehash: b1dffae1543e2c896dc8461048f94d5724c6dc00
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93731573"
---
# <span data-ttu-id="d8cd8-101">New-AzAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="d8cd8-101">New-AzAutomationConnection</span></span>

## <span data-ttu-id="d8cd8-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="d8cd8-102">SYNOPSIS</span></span>
<span data-ttu-id="d8cd8-103">Создает подключение автоматизации.</span><span class="sxs-lookup"><span data-stu-id="d8cd8-103">Creates an Automation connection.</span></span>

## <span data-ttu-id="d8cd8-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="d8cd8-104">SYNTAX</span></span>

```
New-AzAutomationConnection [-Name] <String> [-ConnectionTypeName] <String>
 [-ConnectionFieldValues] <IDictionary> [-Description <String>] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d8cd8-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d8cd8-105">DESCRIPTION</span></span>
<span data-ttu-id="d8cd8-106">Командлет **New-AzAutomationConnection** создает подключение в службе автоматизации Azure.</span><span class="sxs-lookup"><span data-stu-id="d8cd8-106">The **New-AzAutomationConnection** cmdlet creates a connection in Azure Automation.</span></span>

## <span data-ttu-id="d8cd8-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="d8cd8-107">EXAMPLES</span></span>

### <span data-ttu-id="d8cd8-108">Пример 1: создание подключения</span><span class="sxs-lookup"><span data-stu-id="d8cd8-108">Example 1: Create a connection</span></span>
```
PS C:\>$FieldValues = @{"AutomationCertificateName"="ContosoCertificate";"SubscriptionID"="81b59010-dc55-45b7-89cd-5ca26db62472"}
PS C:\> New-AzAutomationConnection -Name "Connection12" -ConnectionTypeName Azure -ConnectionFieldValues $FieldValues -ResourceGroupName "ResourceGroup01" -AutomationAccountName "AutomationAccount01"
```

<span data-ttu-id="d8cd8-109">Первая команда назначает хэш-таблицу значений полей переменной $FieldValue.</span><span class="sxs-lookup"><span data-stu-id="d8cd8-109">The first command assigns a hash table of field values to the $FieldValue variable.</span></span>
<span data-ttu-id="d8cd8-110">Вторая команда создает подключение Azure с именем Connection12 в учетной записи автоматизации с именем AutomationAccount01.</span><span class="sxs-lookup"><span data-stu-id="d8cd8-110">The second command creates an Azure connection named Connection12 in the Automation account named AutomationAccount01.</span></span>
<span data-ttu-id="d8cd8-111">Команда использует значения полей подключения в $FieldValues.</span><span class="sxs-lookup"><span data-stu-id="d8cd8-111">The command uses the connection field values in $FieldValues.</span></span>

## <span data-ttu-id="d8cd8-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="d8cd8-112">PARAMETERS</span></span>

### <span data-ttu-id="d8cd8-113">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="d8cd8-113">-AutomationAccountName</span></span>
<span data-ttu-id="d8cd8-114">Указывает имя учетной записи автоматизации, для которой этот командлет создает подключение.</span><span class="sxs-lookup"><span data-stu-id="d8cd8-114">Specifies the name of the Automation account for which this cmdlet creates a connection.</span></span>

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

### <span data-ttu-id="d8cd8-115">-ConnectionFieldValues</span><span class="sxs-lookup"><span data-stu-id="d8cd8-115">-ConnectionFieldValues</span></span>
<span data-ttu-id="d8cd8-116">Указывает хэш-таблицу, которая содержит пары "ключ-значение".</span><span class="sxs-lookup"><span data-stu-id="d8cd8-116">Specifies a hash table that contains key/value pairs.</span></span>
<span data-ttu-id="d8cd8-117">Ключи представляют поля соединения для указанного типа подключения.</span><span class="sxs-lookup"><span data-stu-id="d8cd8-117">The keys represent the connection fields for the specified connection type.</span></span>
<span data-ttu-id="d8cd8-118">Значения представляют конкретные значения каждого поля соединения для экземпляра Connection.</span><span class="sxs-lookup"><span data-stu-id="d8cd8-118">The values represent the specific values of each connection field for the connection instance.</span></span>

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

### <span data-ttu-id="d8cd8-119">-ConnectionTypeName</span><span class="sxs-lookup"><span data-stu-id="d8cd8-119">-ConnectionTypeName</span></span>
<span data-ttu-id="d8cd8-120">Указывает имя типа подключения.</span><span class="sxs-lookup"><span data-stu-id="d8cd8-120">Specifies the name of the connection type.</span></span>

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

### <span data-ttu-id="d8cd8-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d8cd8-121">-DefaultProfile</span></span>
<span data-ttu-id="d8cd8-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="d8cd8-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d8cd8-123">-Описание</span><span class="sxs-lookup"><span data-stu-id="d8cd8-123">-Description</span></span>
<span data-ttu-id="d8cd8-124">Задает описание подключения.</span><span class="sxs-lookup"><span data-stu-id="d8cd8-124">Specifies a description for the connection.</span></span>

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

### <span data-ttu-id="d8cd8-125">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="d8cd8-125">-Name</span></span>
<span data-ttu-id="d8cd8-126">Задает имя для подключения.</span><span class="sxs-lookup"><span data-stu-id="d8cd8-126">Specifies a name for the connection.</span></span>

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

### <span data-ttu-id="d8cd8-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d8cd8-127">-ResourceGroupName</span></span>
<span data-ttu-id="d8cd8-128">Указывает имя группы ресурсов, для которой этот командлет создает подключение.</span><span class="sxs-lookup"><span data-stu-id="d8cd8-128">Specifies the name of the resource group for which this cmdlet creates a connection.</span></span>

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

### <span data-ttu-id="d8cd8-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d8cd8-129">CommonParameters</span></span>
<span data-ttu-id="d8cd8-130">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="d8cd8-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d8cd8-131">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d8cd8-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d8cd8-132">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="d8cd8-132">INPUTS</span></span>

### <span data-ttu-id="d8cd8-133">System. String</span><span class="sxs-lookup"><span data-stu-id="d8cd8-133">System.String</span></span>

### <span data-ttu-id="d8cd8-134">System. Collections. IDictionary</span><span class="sxs-lookup"><span data-stu-id="d8cd8-134">System.Collections.IDictionary</span></span>

## <span data-ttu-id="d8cd8-135">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="d8cd8-135">OUTPUTS</span></span>

### <span data-ttu-id="d8cd8-136">Microsoft. Azure. Commands. Automation. Model. Connection</span><span class="sxs-lookup"><span data-stu-id="d8cd8-136">Microsoft.Azure.Commands.Automation.Model.Connection</span></span>

## <span data-ttu-id="d8cd8-137">Пуск</span><span class="sxs-lookup"><span data-stu-id="d8cd8-137">NOTES</span></span>

## <span data-ttu-id="d8cd8-138">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d8cd8-138">RELATED LINKS</span></span>

[<span data-ttu-id="d8cd8-139">Get-AzAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="d8cd8-139">Get-AzAutomationConnection</span></span>](./Get-AzAutomationConnection.md)

[<span data-ttu-id="d8cd8-140">Remove-AzAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="d8cd8-140">Remove-AzAutomationConnection</span></span>](./Remove-AzAutomationConnection.md)


