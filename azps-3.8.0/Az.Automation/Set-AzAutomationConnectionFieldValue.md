---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: CA25260C-D0BF-4F9C-A846-9D9B6C48CE8A
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/set-azautomationconnectionfieldvalue
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Set-AzAutomationConnectionFieldValue.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Set-AzAutomationConnectionFieldValue.md
ms.openlocfilehash: 2df58153b2617a8ad62b0e46544128fa47a462b5
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "93911905"
---
# <span data-ttu-id="2e7b8-101">Set-AzAutomationConnectionFieldValue</span><span class="sxs-lookup"><span data-stu-id="2e7b8-101">Set-AzAutomationConnectionFieldValue</span></span>

## <span data-ttu-id="2e7b8-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="2e7b8-102">SYNOPSIS</span></span>
<span data-ttu-id="2e7b8-103">Изменяет значение поля в соединении автоматизации.</span><span class="sxs-lookup"><span data-stu-id="2e7b8-103">Modifies the value of a field in an Automation connection.</span></span>

## <span data-ttu-id="2e7b8-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="2e7b8-104">SYNTAX</span></span>

```
Set-AzAutomationConnectionFieldValue [-Name] <String> -ConnectionFieldName <String> -Value <Object>
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="2e7b8-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="2e7b8-105">DESCRIPTION</span></span>
<span data-ttu-id="2e7b8-106">Командлет **Set-AzAutomationConnectionFieldValue** изменяет значение поля в соединении в службе автоматизации Azure.</span><span class="sxs-lookup"><span data-stu-id="2e7b8-106">The **Set-AzAutomationConnectionFieldValue** cmdlet modifies the value of a field in a connection in Azure Automation.</span></span>

## <span data-ttu-id="2e7b8-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="2e7b8-107">EXAMPLES</span></span>

### <span data-ttu-id="2e7b8-108">Пример 1: изменение значения поля в соединении</span><span class="sxs-lookup"><span data-stu-id="2e7b8-108">Example 1: Change a field value in a connection</span></span>
```
PS C:\>Set-AzAutomationConnectionFieldValue -Name "ContosoConnection" -ConnectionFieldName "SubscriptionID" -Value "b53ec456-3494-4847-8f2b-180901c51050" -ResourceGroupName "ResourceGroup01" -AutomationAccountName "AutomationAccount01"
```

<span data-ttu-id="2e7b8-109">Эта команда изменяет идентификатор подписки для подключения Azure с именем ContosoConnection в учетной записи автоматизации с именем AutomationAccount01.</span><span class="sxs-lookup"><span data-stu-id="2e7b8-109">This command changes the subscription ID for the Azure connection named ContosoConnection in the Automation account named AutomationAccount01.</span></span>

## <span data-ttu-id="2e7b8-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="2e7b8-110">PARAMETERS</span></span>

### <span data-ttu-id="2e7b8-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="2e7b8-111">-AutomationAccountName</span></span>
<span data-ttu-id="2e7b8-112">Указывает имя учетной записи автоматизации, для которой этот командлет изменяет поле в соединении.</span><span class="sxs-lookup"><span data-stu-id="2e7b8-112">Specifies the name of the Automation account for which this cmdlet modifies a field in a connection.</span></span>

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

### <span data-ttu-id="2e7b8-113">-ConnectionFieldName</span><span class="sxs-lookup"><span data-stu-id="2e7b8-113">-ConnectionFieldName</span></span>
<span data-ttu-id="2e7b8-114">Задает имя поля, которое изменяет этот командлет.</span><span class="sxs-lookup"><span data-stu-id="2e7b8-114">Specifies a name for the field that this cmdlet modifies.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2e7b8-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2e7b8-115">-DefaultProfile</span></span>
<span data-ttu-id="2e7b8-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="2e7b8-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2e7b8-117">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="2e7b8-117">-Name</span></span>
<span data-ttu-id="2e7b8-118">Указывает имя подключения, для которого этот командлет изменяет поле.</span><span class="sxs-lookup"><span data-stu-id="2e7b8-118">Specifies a name for the connection for which this cmdlet modifies a field.</span></span>

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

### <span data-ttu-id="2e7b8-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2e7b8-119">-ResourceGroupName</span></span>
<span data-ttu-id="2e7b8-120">Указывает имя группы ресурсов, для которой этот командлет изменяет поле в соединении.</span><span class="sxs-lookup"><span data-stu-id="2e7b8-120">Specifies the name of the resource group for which this cmdlet modifies a field in a connection.</span></span>

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

### <span data-ttu-id="2e7b8-121">-Value (значение)</span><span class="sxs-lookup"><span data-stu-id="2e7b8-121">-Value</span></span>
<span data-ttu-id="2e7b8-122">Задает значение, которое нужно изменить, в поле Connection (соединение).</span><span class="sxs-lookup"><span data-stu-id="2e7b8-122">Specifies a value to modify in the connection field.</span></span>

```yaml
Type: System.Object
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2e7b8-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2e7b8-123">CommonParameters</span></span>
<span data-ttu-id="2e7b8-124">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="2e7b8-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2e7b8-125">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2e7b8-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2e7b8-126">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="2e7b8-126">INPUTS</span></span>

### <span data-ttu-id="2e7b8-127">System. String</span><span class="sxs-lookup"><span data-stu-id="2e7b8-127">System.String</span></span>

### <span data-ttu-id="2e7b8-128">System. Object</span><span class="sxs-lookup"><span data-stu-id="2e7b8-128">System.Object</span></span>

## <span data-ttu-id="2e7b8-129">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="2e7b8-129">OUTPUTS</span></span>

### <span data-ttu-id="2e7b8-130">Microsoft. Azure. Commands. Automation. Model. Connection</span><span class="sxs-lookup"><span data-stu-id="2e7b8-130">Microsoft.Azure.Commands.Automation.Model.Connection</span></span>

## <span data-ttu-id="2e7b8-131">Пуск</span><span class="sxs-lookup"><span data-stu-id="2e7b8-131">NOTES</span></span>

## <span data-ttu-id="2e7b8-132">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="2e7b8-132">RELATED LINKS</span></span>

[<span data-ttu-id="2e7b8-133">New-AzAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="2e7b8-133">New-AzAutomationConnection</span></span>](./New-AzAutomationConnection.md)


