---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 055526FA-5DB7-4F1D-81B3-5D9753283FE2
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/new-azautomationkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationKey.md
ms.openlocfilehash: 1d0587ae9d1d45de4f08b71baa48ebb5e1633a36
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93727802"
---
# <span data-ttu-id="ad01e-101">New-AzAutomationKey</span><span class="sxs-lookup"><span data-stu-id="ad01e-101">New-AzAutomationKey</span></span>

## <span data-ttu-id="ad01e-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="ad01e-102">SYNOPSIS</span></span>
<span data-ttu-id="ad01e-103">Повторное создание регистрационных ключей для учетной записи автоматизации.</span><span class="sxs-lookup"><span data-stu-id="ad01e-103">Regenerates registration keys for an Automation account.</span></span>

## <span data-ttu-id="ad01e-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="ad01e-104">SYNTAX</span></span>

```
New-AzAutomationKey [-KeyType] <String> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ad01e-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ad01e-105">DESCRIPTION</span></span>
<span data-ttu-id="ad01e-106">Командлет **New-AzAutomationKey** заново создает ключи регистрации для учетной записи службы автоматизации Azure.</span><span class="sxs-lookup"><span data-stu-id="ad01e-106">The **New-AzAutomationKey** cmdlet regenerates registration keys for an Azure Automation account.</span></span>

## <span data-ttu-id="ad01e-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="ad01e-107">EXAMPLES</span></span>

### <span data-ttu-id="ad01e-108">Пример 1: повторное создание ключа для учетной записи автоматизации</span><span class="sxs-lookup"><span data-stu-id="ad01e-108">Example 1: Regenerate a key for an Automation account</span></span>
```
PS C:\>New-AzAutomationKey -KeyType Primary -ResourceGroup "ResourceGroup01" -AutomationAccountName "AutomationAccount01"
```

<span data-ttu-id="ad01e-109">Эта команда повторно создает первичный ключ для учетной записи службы автоматизации Azure с именем AutomationAccount01 в группе ресурсов с именем ResourceGroup01.</span><span class="sxs-lookup"><span data-stu-id="ad01e-109">This command regenerates the primary key for the Azure Automation account named AutomationAccount01 in the resource group named ResourceGroup01.</span></span>

## <span data-ttu-id="ad01e-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="ad01e-110">PARAMETERS</span></span>

### <span data-ttu-id="ad01e-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="ad01e-111">-AutomationAccountName</span></span>
<span data-ttu-id="ad01e-112">Указывает имя учетной записи автоматизации, для которой этот командлет повторно генерирует ключи.</span><span class="sxs-lookup"><span data-stu-id="ad01e-112">Specifies the name of an Automation account for which this cmdlet regenerates keys.</span></span>

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

### <span data-ttu-id="ad01e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ad01e-113">-DefaultProfile</span></span>
<span data-ttu-id="ad01e-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="ad01e-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ad01e-115">-KeyType</span><span class="sxs-lookup"><span data-stu-id="ad01e-115">-KeyType</span></span>
<span data-ttu-id="ad01e-116">Указывает тип регистрационного ключа агента.</span><span class="sxs-lookup"><span data-stu-id="ad01e-116">Specifies the type of the agent registration key.</span></span>
<span data-ttu-id="ad01e-117">Допустимые значения:</span><span class="sxs-lookup"><span data-stu-id="ad01e-117">Valid values are:</span></span> 
- <span data-ttu-id="ad01e-118">Главная</span><span class="sxs-lookup"><span data-stu-id="ad01e-118">Primary</span></span> 
- <span data-ttu-id="ad01e-119">Запас</span><span class="sxs-lookup"><span data-stu-id="ad01e-119">Secondary</span></span>

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

### <span data-ttu-id="ad01e-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ad01e-120">-ResourceGroupName</span></span>
<span data-ttu-id="ad01e-121">Указывает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="ad01e-121">Specifies the name of a resource group.</span></span>
<span data-ttu-id="ad01e-122">Этот командлет повторно создает ключи для учетной записи автоматизации в группе ресурсов, которую указывает этот параметр.</span><span class="sxs-lookup"><span data-stu-id="ad01e-122">This cmdlet regenerates keys for an Automation account in the resource group that this parameter specifies.</span></span>

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

### <span data-ttu-id="ad01e-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ad01e-123">CommonParameters</span></span>
<span data-ttu-id="ad01e-124">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="ad01e-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ad01e-125">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ad01e-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ad01e-126">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="ad01e-126">INPUTS</span></span>

### <span data-ttu-id="ad01e-127">System. String</span><span class="sxs-lookup"><span data-stu-id="ad01e-127">System.String</span></span>

## <span data-ttu-id="ad01e-128">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="ad01e-128">OUTPUTS</span></span>

### <span data-ttu-id="ad01e-129">Microsoft. Azure. Commands. Automation. Model. AgentRegistration</span><span class="sxs-lookup"><span data-stu-id="ad01e-129">Microsoft.Azure.Commands.Automation.Model.AgentRegistration</span></span>

## <span data-ttu-id="ad01e-130">Пуск</span><span class="sxs-lookup"><span data-stu-id="ad01e-130">NOTES</span></span>

## <span data-ttu-id="ad01e-131">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ad01e-131">RELATED LINKS</span></span>
