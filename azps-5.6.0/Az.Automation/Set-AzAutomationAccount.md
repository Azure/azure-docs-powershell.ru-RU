---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: B1897EFC-0184-4A8B-B8E4-203CC8E3B179
online version: https://docs.microsoft.com/powershell/module/az.automation/set-azautomationaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Set-AzAutomationAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Set-AzAutomationAccount.md
ms.openlocfilehash: bc810da3cd43a18506160d03e6c172eb272bd797
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102009832"
---
# <span data-ttu-id="6a137-101">Set-AzAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="6a137-101">Set-AzAutomationAccount</span></span>

## <span data-ttu-id="6a137-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6a137-102">SYNOPSIS</span></span>
<span data-ttu-id="6a137-103">Изменяет учетную запись автоматизации.</span><span class="sxs-lookup"><span data-stu-id="6a137-103">Modifies an Automation account.</span></span>

## <span data-ttu-id="6a137-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="6a137-104">SYNTAX</span></span>

```
Set-AzAutomationAccount [-ResourceGroupName] <String> [-Name] <String> [-Plan <String>] [-Tags <IDictionary>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6a137-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="6a137-105">DESCRIPTION</span></span>
<span data-ttu-id="6a137-106">**Cmdlet Set-AzAutomationAccount** изменяет учетную запись автоматизации Azure.</span><span class="sxs-lookup"><span data-stu-id="6a137-106">The **Set-AzAutomationAccount** cmdlet modifies an Azure Automation account.</span></span>
<span data-ttu-id="6a137-107">Дополнительные сведения об учетных записях автоматизации см. в New-AzAutomationAccount>.</span><span class="sxs-lookup"><span data-stu-id="6a137-107">For more information about Automation accounts, see the New-AzAutomationAccount cmdlet.</span></span>

## <span data-ttu-id="6a137-108">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="6a137-108">EXAMPLES</span></span>

### <span data-ttu-id="6a137-109">Пример 1. Настройка тегов для учетной записи автоматизации</span><span class="sxs-lookup"><span data-stu-id="6a137-109">Example 1: Set the tags for an Automation account</span></span>
```
PS C:\>$Tags = @{"tag01"="value01";"tag02"="value02"}
PS C:\> Set-AzAutomationAccount -Name "AutomationAccount01" -ResourceGroupName "ResourceGroup01" -Tags $Tags
```

<span data-ttu-id="6a137-110">Первая команда назначает две пары ключей и значений переменной $Tags.</span><span class="sxs-lookup"><span data-stu-id="6a137-110">The first command assigns two key/value pairs to the $Tags variable.</span></span>
<span data-ttu-id="6a137-111">Вторая команда задает теги в $Tags для учетной записи автоматизации с именем AutomationAccount01.</span><span class="sxs-lookup"><span data-stu-id="6a137-111">The second command sets tags in $Tags for the Automation account named AutomationAccount01.</span></span>

### <span data-ttu-id="6a137-112">Пример 2. Изменение плана для учетной записи автоматизации</span><span class="sxs-lookup"><span data-stu-id="6a137-112">Example 2: Change the plan for an Automation account</span></span>
```
PS C:\>Set-AzAutomationAccount -Name "AutomationAccount01" -ResourceGroupName "ResourceGroup01" -Plan Basic
```

<span data-ttu-id="6a137-113">Эта команда изменяет план на "Базовая" для учетной записи автоматизации с именем AutomationAccount01.</span><span class="sxs-lookup"><span data-stu-id="6a137-113">This command changes the plan to Basic for the Automation account named AutomationAccount01.</span></span>

## <span data-ttu-id="6a137-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6a137-114">PARAMETERS</span></span>

### <span data-ttu-id="6a137-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6a137-115">-DefaultProfile</span></span>
<span data-ttu-id="6a137-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="6a137-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6a137-117">-Name</span><span class="sxs-lookup"><span data-stu-id="6a137-117">-Name</span></span>
<span data-ttu-id="6a137-118">Указывает имя учетной записи автоматизации, которую изменяет этот cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6a137-118">Specifies the name of the Automation account that this cmdlet modifies.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AutomationAccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6a137-119">-Plan</span><span class="sxs-lookup"><span data-stu-id="6a137-119">-Plan</span></span>
<span data-ttu-id="6a137-120">Определяет план для учетной записи автоматизации.</span><span class="sxs-lookup"><span data-stu-id="6a137-120">Specifies the plan for the Automation account.</span></span>
<span data-ttu-id="6a137-121">Допустимые значения:</span><span class="sxs-lookup"><span data-stu-id="6a137-121">Valid values are:</span></span>
- <span data-ttu-id="6a137-122">Базовая</span><span class="sxs-lookup"><span data-stu-id="6a137-122">Basic</span></span>
- <span data-ttu-id="6a137-123">Бесплатно</span><span class="sxs-lookup"><span data-stu-id="6a137-123">Free</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Free, Basic

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6a137-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6a137-124">-ResourceGroupName</span></span>
<span data-ttu-id="6a137-125">Имя группы ресурсов, которая содержит учетную запись автоматизации, которую изменяет этот cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6a137-125">Specifies the name of a resource group that contains the Automation account that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="6a137-126">-Теги</span><span class="sxs-lookup"><span data-stu-id="6a137-126">-Tags</span></span>
<span data-ttu-id="6a137-127">Пары "ключевое значение" в виде hash table.</span><span class="sxs-lookup"><span data-stu-id="6a137-127">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="6a137-128">Например: @{key0="value0";key1=$null;key2="value2"}</span><span class="sxs-lookup"><span data-stu-id="6a137-128">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.IDictionary
Parameter Sets: (All)
Aliases: Tag

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6a137-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6a137-129">CommonParameters</span></span>
<span data-ttu-id="6a137-130">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6a137-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6a137-131">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6a137-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6a137-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="6a137-132">INPUTS</span></span>

### <span data-ttu-id="6a137-133">System.String</span><span class="sxs-lookup"><span data-stu-id="6a137-133">System.String</span></span>

### <span data-ttu-id="6a137-134">System.Collections.IDictionary</span><span class="sxs-lookup"><span data-stu-id="6a137-134">System.Collections.IDictionary</span></span>

## <span data-ttu-id="6a137-135">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="6a137-135">OUTPUTS</span></span>

### <span data-ttu-id="6a137-136">Microsoft.Azure.Commands.Automation.Model.AutomationAccount</span><span class="sxs-lookup"><span data-stu-id="6a137-136">Microsoft.Azure.Commands.Automation.Model.AutomationAccount</span></span>

## <span data-ttu-id="6a137-137">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="6a137-137">NOTES</span></span>

## <span data-ttu-id="6a137-138">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="6a137-138">RELATED LINKS</span></span>

[<span data-ttu-id="6a137-139">Get-AzAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="6a137-139">Get-AzAutomationAccount</span></span>](./Get-AzAutomationAccount.md)

[<span data-ttu-id="6a137-140">New-AzAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="6a137-140">New-AzAutomationAccount</span></span>](./New-AzAutomationAccount.md)

[<span data-ttu-id="6a137-141">Remove-AzAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="6a137-141">Remove-AzAutomationAccount</span></span>](./Remove-AzAutomationAccount.md)
