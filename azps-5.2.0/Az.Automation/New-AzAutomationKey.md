---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 055526FA-5DB7-4F1D-81B3-5D9753283FE2
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/new-azautomationkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationKey.md
ms.openlocfilehash: ed10bd42fb52515cb05adadfc69ee4f1620150e3
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98418516"
---
# <span data-ttu-id="89eb6-101">New-AzAutomationKey</span><span class="sxs-lookup"><span data-stu-id="89eb6-101">New-AzAutomationKey</span></span>

## <span data-ttu-id="89eb6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="89eb6-102">SYNOPSIS</span></span>
<span data-ttu-id="89eb6-103">Повторно сгенерирует ключи регистрации для учетной записи автоматизации.</span><span class="sxs-lookup"><span data-stu-id="89eb6-103">Regenerates registration keys for an Automation account.</span></span>

## <span data-ttu-id="89eb6-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="89eb6-104">SYNTAX</span></span>

```
New-AzAutomationKey [-KeyType] <String> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="89eb6-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="89eb6-105">DESCRIPTION</span></span>
<span data-ttu-id="89eb6-106">Для учетной записи автоматизации Azure сгенерирует ключи регистрации для новой учетной записи **AzAutomationKey.**</span><span class="sxs-lookup"><span data-stu-id="89eb6-106">The **New-AzAutomationKey** cmdlet regenerates registration keys for an Azure Automation account.</span></span>

## <span data-ttu-id="89eb6-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="89eb6-107">EXAMPLES</span></span>

### <span data-ttu-id="89eb6-108">Пример 1. Повторное сгенерировать ключ для учетной записи автоматизации</span><span class="sxs-lookup"><span data-stu-id="89eb6-108">Example 1: Regenerate a key for an Automation account</span></span>
```
PS C:\>New-AzAutomationKey -KeyType Primary -ResourceGroup "ResourceGroup01" -AutomationAccountName "AutomationAccount01"
```

<span data-ttu-id="89eb6-109">Эта команда повторно сгенерирует первичный ключ для учетной записи автоматизации Azure с именем AutomationAccount01 в группе ресурсов ResourceGroup01.</span><span class="sxs-lookup"><span data-stu-id="89eb6-109">This command regenerates the primary key for the Azure Automation account named AutomationAccount01 in the resource group named ResourceGroup01.</span></span>

## <span data-ttu-id="89eb6-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="89eb6-110">PARAMETERS</span></span>

### <span data-ttu-id="89eb6-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="89eb6-111">-AutomationAccountName</span></span>
<span data-ttu-id="89eb6-112">Указывает имя учетной записи автоматизации, для которой этот cmdlet повторно сгенерирует ключи.</span><span class="sxs-lookup"><span data-stu-id="89eb6-112">Specifies the name of an Automation account for which this cmdlet regenerates keys.</span></span>

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

### <span data-ttu-id="89eb6-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="89eb6-113">-DefaultProfile</span></span>
<span data-ttu-id="89eb6-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="89eb6-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="89eb6-115">-KeyType</span><span class="sxs-lookup"><span data-stu-id="89eb6-115">-KeyType</span></span>
<span data-ttu-id="89eb6-116">Определяет тип регистрационного ключа агента.</span><span class="sxs-lookup"><span data-stu-id="89eb6-116">Specifies the type of the agent registration key.</span></span>
<span data-ttu-id="89eb6-117">Допустимые значения:</span><span class="sxs-lookup"><span data-stu-id="89eb6-117">Valid values are:</span></span> 
- <span data-ttu-id="89eb6-118">Primary</span><span class="sxs-lookup"><span data-stu-id="89eb6-118">Primary</span></span> 
- <span data-ttu-id="89eb6-119">Secondary</span><span class="sxs-lookup"><span data-stu-id="89eb6-119">Secondary</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Primary, Secondary

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="89eb6-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="89eb6-120">-ResourceGroupName</span></span>
<span data-ttu-id="89eb6-121">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="89eb6-121">Specifies the name of a resource group.</span></span>
<span data-ttu-id="89eb6-122">Этот cmdlet повторно сгенерирует ключи для учетной записи Автоматизации в группе ресурсов, указанной этим параметром.</span><span class="sxs-lookup"><span data-stu-id="89eb6-122">This cmdlet regenerates keys for an Automation account in the resource group that this parameter specifies.</span></span>

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

### <span data-ttu-id="89eb6-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="89eb6-123">CommonParameters</span></span>
<span data-ttu-id="89eb6-124">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="89eb6-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="89eb6-125">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="89eb6-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="89eb6-126">INPUTS</span><span class="sxs-lookup"><span data-stu-id="89eb6-126">INPUTS</span></span>

### <span data-ttu-id="89eb6-127">System.String</span><span class="sxs-lookup"><span data-stu-id="89eb6-127">System.String</span></span>

## <span data-ttu-id="89eb6-128">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="89eb6-128">OUTPUTS</span></span>

### <span data-ttu-id="89eb6-129">Microsoft.Azure.Commands.Automation.Model.AgentRegistration</span><span class="sxs-lookup"><span data-stu-id="89eb6-129">Microsoft.Azure.Commands.Automation.Model.AgentRegistration</span></span>

## <span data-ttu-id="89eb6-130">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="89eb6-130">NOTES</span></span>

## <span data-ttu-id="89eb6-131">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="89eb6-131">RELATED LINKS</span></span>
