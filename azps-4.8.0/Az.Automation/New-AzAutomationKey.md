---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 055526FA-5DB7-4F1D-81B3-5D9753283FE2
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/new-azautomationkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationKey.md
ms.openlocfilehash: ed10bd42fb52515cb05adadfc69ee4f1620150e3
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94077935"
---
# <span data-ttu-id="ba124-101">New-AzAutomationKey</span><span class="sxs-lookup"><span data-stu-id="ba124-101">New-AzAutomationKey</span></span>

## <span data-ttu-id="ba124-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="ba124-102">SYNOPSIS</span></span>
<span data-ttu-id="ba124-103">Повторное создание регистрационных ключей для учетной записи автоматизации.</span><span class="sxs-lookup"><span data-stu-id="ba124-103">Regenerates registration keys for an Automation account.</span></span>

## <span data-ttu-id="ba124-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="ba124-104">SYNTAX</span></span>

```
New-AzAutomationKey [-KeyType] <String> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ba124-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ba124-105">DESCRIPTION</span></span>
<span data-ttu-id="ba124-106">Командлет **New-AzAutomationKey** заново создает ключи регистрации для учетной записи службы автоматизации Azure.</span><span class="sxs-lookup"><span data-stu-id="ba124-106">The **New-AzAutomationKey** cmdlet regenerates registration keys for an Azure Automation account.</span></span>

## <span data-ttu-id="ba124-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="ba124-107">EXAMPLES</span></span>

### <span data-ttu-id="ba124-108">Пример 1: повторное создание ключа для учетной записи автоматизации</span><span class="sxs-lookup"><span data-stu-id="ba124-108">Example 1: Regenerate a key for an Automation account</span></span>
```
PS C:\>New-AzAutomationKey -KeyType Primary -ResourceGroup "ResourceGroup01" -AutomationAccountName "AutomationAccount01"
```

<span data-ttu-id="ba124-109">Эта команда повторно создает первичный ключ для учетной записи службы автоматизации Azure с именем AutomationAccount01 в группе ресурсов с именем ResourceGroup01.</span><span class="sxs-lookup"><span data-stu-id="ba124-109">This command regenerates the primary key for the Azure Automation account named AutomationAccount01 in the resource group named ResourceGroup01.</span></span>

## <span data-ttu-id="ba124-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="ba124-110">PARAMETERS</span></span>

### <span data-ttu-id="ba124-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="ba124-111">-AutomationAccountName</span></span>
<span data-ttu-id="ba124-112">Указывает имя учетной записи автоматизации, для которой этот командлет повторно генерирует ключи.</span><span class="sxs-lookup"><span data-stu-id="ba124-112">Specifies the name of an Automation account for which this cmdlet regenerates keys.</span></span>

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

### <span data-ttu-id="ba124-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ba124-113">-DefaultProfile</span></span>
<span data-ttu-id="ba124-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="ba124-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ba124-115">-KeyType</span><span class="sxs-lookup"><span data-stu-id="ba124-115">-KeyType</span></span>
<span data-ttu-id="ba124-116">Указывает тип регистрационного ключа агента.</span><span class="sxs-lookup"><span data-stu-id="ba124-116">Specifies the type of the agent registration key.</span></span>
<span data-ttu-id="ba124-117">Допустимые значения:</span><span class="sxs-lookup"><span data-stu-id="ba124-117">Valid values are:</span></span> 
- <span data-ttu-id="ba124-118">Главная</span><span class="sxs-lookup"><span data-stu-id="ba124-118">Primary</span></span> 
- <span data-ttu-id="ba124-119">Запас</span><span class="sxs-lookup"><span data-stu-id="ba124-119">Secondary</span></span>

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

### <span data-ttu-id="ba124-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ba124-120">-ResourceGroupName</span></span>
<span data-ttu-id="ba124-121">Указывает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="ba124-121">Specifies the name of a resource group.</span></span>
<span data-ttu-id="ba124-122">Этот командлет повторно создает ключи для учетной записи автоматизации в группе ресурсов, которую указывает этот параметр.</span><span class="sxs-lookup"><span data-stu-id="ba124-122">This cmdlet regenerates keys for an Automation account in the resource group that this parameter specifies.</span></span>

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

### <span data-ttu-id="ba124-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ba124-123">CommonParameters</span></span>
<span data-ttu-id="ba124-124">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="ba124-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ba124-125">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ba124-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ba124-126">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="ba124-126">INPUTS</span></span>

### <span data-ttu-id="ba124-127">System. String</span><span class="sxs-lookup"><span data-stu-id="ba124-127">System.String</span></span>

## <span data-ttu-id="ba124-128">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="ba124-128">OUTPUTS</span></span>

### <span data-ttu-id="ba124-129">Microsoft. Azure. Commands. Automation. Model. AgentRegistration</span><span class="sxs-lookup"><span data-stu-id="ba124-129">Microsoft.Azure.Commands.Automation.Model.AgentRegistration</span></span>

## <span data-ttu-id="ba124-130">Пуск</span><span class="sxs-lookup"><span data-stu-id="ba124-130">NOTES</span></span>

## <span data-ttu-id="ba124-131">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ba124-131">RELATED LINKS</span></span>