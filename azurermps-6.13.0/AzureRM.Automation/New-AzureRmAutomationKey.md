---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 055526FA-5DB7-4F1D-81B3-5D9753283FE2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/new-azurermautomationkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/New-AzureRmAutomationKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/New-AzureRmAutomationKey.md
ms.openlocfilehash: 8bd043f11294b2290a5f54289232bc826c1f0d88
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93556855"
---
# <span data-ttu-id="957b4-101">New-AzureRmAutomationKey</span><span class="sxs-lookup"><span data-stu-id="957b4-101">New-AzureRmAutomationKey</span></span>

## <span data-ttu-id="957b4-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="957b4-102">SYNOPSIS</span></span>
<span data-ttu-id="957b4-103">Повторное создание регистрационных ключей для учетной записи автоматизации.</span><span class="sxs-lookup"><span data-stu-id="957b4-103">Regenerates registration keys for an Automation account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="957b4-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="957b4-104">SYNTAX</span></span>

```
New-AzureRmAutomationKey [-KeyType] <String> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="957b4-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="957b4-105">DESCRIPTION</span></span>
<span data-ttu-id="957b4-106">Командлет **New-AzureRmAutomationKey** заново создает ключи регистрации для учетной записи службы автоматизации Azure.</span><span class="sxs-lookup"><span data-stu-id="957b4-106">The **New-AzureRmAutomationKey** cmdlet regenerates registration keys for an Azure Automation account.</span></span>

## <span data-ttu-id="957b4-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="957b4-107">EXAMPLES</span></span>

### <span data-ttu-id="957b4-108">Пример 1: повторное создание ключа для учетной записи автоматизации</span><span class="sxs-lookup"><span data-stu-id="957b4-108">Example 1: Regenerate a key for an Automation account</span></span>
```
PS C:\>New-AzureAutomationKey -KeyType Primary -ResourceGroup "ResourceGroup01" -AutomationAccountName "AutomationAccount01"
```

<span data-ttu-id="957b4-109">Эта команда повторно создает первичный ключ для учетной записи службы автоматизации Azure с именем AutomationAccount01 в группе ресурсов с именем ResourceGroup01.</span><span class="sxs-lookup"><span data-stu-id="957b4-109">This command regenerates the primary key for the Azure Automation account named AutomationAccount01 in the resource group named ResourceGroup01.</span></span>

## <span data-ttu-id="957b4-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="957b4-110">PARAMETERS</span></span>

### <span data-ttu-id="957b4-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="957b4-111">-AutomationAccountName</span></span>
<span data-ttu-id="957b4-112">Указывает имя учетной записи автоматизации, для которой этот командлет повторно генерирует ключи.</span><span class="sxs-lookup"><span data-stu-id="957b4-112">Specifies the name of an Automation account for which this cmdlet regenerates keys.</span></span>

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

### <span data-ttu-id="957b4-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="957b4-113">-DefaultProfile</span></span>
<span data-ttu-id="957b4-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="957b4-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="957b4-115">-KeyType</span><span class="sxs-lookup"><span data-stu-id="957b4-115">-KeyType</span></span>
<span data-ttu-id="957b4-116">Указывает тип регистрационного ключа агента.</span><span class="sxs-lookup"><span data-stu-id="957b4-116">Specifies the type of the agent registration key.</span></span>
<span data-ttu-id="957b4-117">Допустимые значения:</span><span class="sxs-lookup"><span data-stu-id="957b4-117">Valid values are:</span></span> 
- <span data-ttu-id="957b4-118">Главная</span><span class="sxs-lookup"><span data-stu-id="957b4-118">Primary</span></span> 
- <span data-ttu-id="957b4-119">Запас</span><span class="sxs-lookup"><span data-stu-id="957b4-119">Secondary</span></span>

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

### <span data-ttu-id="957b4-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="957b4-120">-ResourceGroupName</span></span>
<span data-ttu-id="957b4-121">Указывает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="957b4-121">Specifies the name of a resource group.</span></span>
<span data-ttu-id="957b4-122">Этот командлет повторно создает ключи для учетной записи автоматизации в группе ресурсов, которую указывает этот параметр.</span><span class="sxs-lookup"><span data-stu-id="957b4-122">This cmdlet regenerates keys for an Automation account in the resource group that this parameter specifies.</span></span>

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

### <span data-ttu-id="957b4-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="957b4-123">CommonParameters</span></span>
<span data-ttu-id="957b4-124">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="957b4-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="957b4-125">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="957b4-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="957b4-126">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="957b4-126">INPUTS</span></span>

### <span data-ttu-id="957b4-127">System. String</span><span class="sxs-lookup"><span data-stu-id="957b4-127">System.String</span></span>

## <span data-ttu-id="957b4-128">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="957b4-128">OUTPUTS</span></span>

### <span data-ttu-id="957b4-129">Microsoft. Azure. Commands. Automation. Model. AgentRegistration</span><span class="sxs-lookup"><span data-stu-id="957b4-129">Microsoft.Azure.Commands.Automation.Model.AgentRegistration</span></span>

## <span data-ttu-id="957b4-130">Пуск</span><span class="sxs-lookup"><span data-stu-id="957b4-130">NOTES</span></span>

## <span data-ttu-id="957b4-131">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="957b4-131">RELATED LINKS</span></span>
