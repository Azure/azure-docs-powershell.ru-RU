---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: CA25260C-D0BF-4F9C-A846-9D9B6C48CE8A
online version: https://docs.microsoft.com/powershell/module/az.automation/set-azautomationconnectionfieldvalue
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Set-AzAutomationConnectionFieldValue.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Set-AzAutomationConnectionFieldValue.md
ms.openlocfilehash: d11b99352d3a3f75c24e47cabfe06e816958fb82
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102004739"
---
# <span data-ttu-id="d8b0c-101">Set-AzAutomationConnectionFieldValue</span><span class="sxs-lookup"><span data-stu-id="d8b0c-101">Set-AzAutomationConnectionFieldValue</span></span>

## <span data-ttu-id="d8b0c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d8b0c-102">SYNOPSIS</span></span>
<span data-ttu-id="d8b0c-103">Изменяет значение поля в соединении автоматизации.</span><span class="sxs-lookup"><span data-stu-id="d8b0c-103">Modifies the value of a field in an Automation connection.</span></span>

## <span data-ttu-id="d8b0c-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="d8b0c-104">SYNTAX</span></span>

```
Set-AzAutomationConnectionFieldValue [-Name] <String> -ConnectionFieldName <String> -Value <Object>
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="d8b0c-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d8b0c-105">DESCRIPTION</span></span>
<span data-ttu-id="d8b0c-106">**Cmdlet Set-AzAutomationConnectionFieldValue** изменяет значение поля в соединении в автоматизации Azure.</span><span class="sxs-lookup"><span data-stu-id="d8b0c-106">The **Set-AzAutomationConnectionFieldValue** cmdlet modifies the value of a field in a connection in Azure Automation.</span></span>

## <span data-ttu-id="d8b0c-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="d8b0c-107">EXAMPLES</span></span>

### <span data-ttu-id="d8b0c-108">Пример 1. Изменение значения поля в соединении</span><span class="sxs-lookup"><span data-stu-id="d8b0c-108">Example 1: Change a field value in a connection</span></span>
```
PS C:\>Set-AzAutomationConnectionFieldValue -Name "ContosoConnection" -ConnectionFieldName "SubscriptionID" -Value "b53ec456-3494-4847-8f2b-180901c51050" -ResourceGroupName "ResourceGroup01" -AutomationAccountName "AutomationAccount01"
```

<span data-ttu-id="d8b0c-109">Эта команда изменяет ИД подписки для подключения Azure ContosoConnection в учетной записи автоматизации с именем AutomationAccount01.</span><span class="sxs-lookup"><span data-stu-id="d8b0c-109">This command changes the subscription ID for the Azure connection named ContosoConnection in the Automation account named AutomationAccount01.</span></span>

## <span data-ttu-id="d8b0c-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d8b0c-110">PARAMETERS</span></span>

### <span data-ttu-id="d8b0c-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="d8b0c-111">-AutomationAccountName</span></span>
<span data-ttu-id="d8b0c-112">Указывает имя учетной записи автоматизации, для которой этот cmdlet изменяет поле в соединении.</span><span class="sxs-lookup"><span data-stu-id="d8b0c-112">Specifies the name of the Automation account for which this cmdlet modifies a field in a connection.</span></span>

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

### <span data-ttu-id="d8b0c-113">-ConnectionFieldName</span><span class="sxs-lookup"><span data-stu-id="d8b0c-113">-ConnectionFieldName</span></span>
<span data-ttu-id="d8b0c-114">Указывает имя поля, которое изменяет этот cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d8b0c-114">Specifies a name for the field that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="d8b0c-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d8b0c-115">-DefaultProfile</span></span>
<span data-ttu-id="d8b0c-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="d8b0c-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d8b0c-117">-Name</span><span class="sxs-lookup"><span data-stu-id="d8b0c-117">-Name</span></span>
<span data-ttu-id="d8b0c-118">Указывает имя подключения, для которого этот cmdlet изменяет поле.</span><span class="sxs-lookup"><span data-stu-id="d8b0c-118">Specifies a name for the connection for which this cmdlet modifies a field.</span></span>

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

### <span data-ttu-id="d8b0c-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d8b0c-119">-ResourceGroupName</span></span>
<span data-ttu-id="d8b0c-120">Имя группы ресурсов, для которой этот cmdlet изменяет поле в соединении.</span><span class="sxs-lookup"><span data-stu-id="d8b0c-120">Specifies the name of the resource group for which this cmdlet modifies a field in a connection.</span></span>

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

### <span data-ttu-id="d8b0c-121">-Значение</span><span class="sxs-lookup"><span data-stu-id="d8b0c-121">-Value</span></span>
<span data-ttu-id="d8b0c-122">Указывает значение, изменяемого в поле подключения.</span><span class="sxs-lookup"><span data-stu-id="d8b0c-122">Specifies a value to modify in the connection field.</span></span>

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

### <span data-ttu-id="d8b0c-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d8b0c-123">CommonParameters</span></span>
<span data-ttu-id="d8b0c-124">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d8b0c-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d8b0c-125">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d8b0c-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d8b0c-126">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d8b0c-126">INPUTS</span></span>

### <span data-ttu-id="d8b0c-127">System.String</span><span class="sxs-lookup"><span data-stu-id="d8b0c-127">System.String</span></span>

### <span data-ttu-id="d8b0c-128">System.Object</span><span class="sxs-lookup"><span data-stu-id="d8b0c-128">System.Object</span></span>

## <span data-ttu-id="d8b0c-129">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="d8b0c-129">OUTPUTS</span></span>

### <span data-ttu-id="d8b0c-130">Microsoft.Azure.Commands.Automation.Model.Connection</span><span class="sxs-lookup"><span data-stu-id="d8b0c-130">Microsoft.Azure.Commands.Automation.Model.Connection</span></span>

## <span data-ttu-id="d8b0c-131">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="d8b0c-131">NOTES</span></span>

## <span data-ttu-id="d8b0c-132">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d8b0c-132">RELATED LINKS</span></span>

[<span data-ttu-id="d8b0c-133">New-AzAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="d8b0c-133">New-AzAutomationConnection</span></span>](./New-AzAutomationConnection.md)


