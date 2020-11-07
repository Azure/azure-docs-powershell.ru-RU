---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: B1897EFC-0184-4A8B-B8E4-203CC8E3B179
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/set-azurermautomationaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Set-AzureRmAutomationAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Set-AzureRmAutomationAccount.md
ms.openlocfilehash: 7a0341221dee0f282508377d1233e30deae1fcee
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93731988"
---
# <span data-ttu-id="35a78-101">Set-AzureRmAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="35a78-101">Set-AzureRmAutomationAccount</span></span>

## <span data-ttu-id="35a78-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="35a78-102">SYNOPSIS</span></span>
<span data-ttu-id="35a78-103">Изменение учетной записи автоматизации.</span><span class="sxs-lookup"><span data-stu-id="35a78-103">Modifies an Automation account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="35a78-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="35a78-104">SYNTAX</span></span>

```
Set-AzureRmAutomationAccount [-ResourceGroupName] <String> [-Name] <String> [-Plan <String>]
 [-Tags <IDictionary>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="35a78-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="35a78-105">DESCRIPTION</span></span>
<span data-ttu-id="35a78-106">Командлет **Set-AzureRmAutomationAccount** изменяет учетную запись службы автоматизации Azure.</span><span class="sxs-lookup"><span data-stu-id="35a78-106">The **Set-AzureRmAutomationAccount** cmdlet modifies an Azure Automation account.</span></span>
<span data-ttu-id="35a78-107">Дополнительные сведения об учетных записях автоматизации можно найти в командлете New-AzureRmAutomationAccount.</span><span class="sxs-lookup"><span data-stu-id="35a78-107">For more information about Automation accounts, see the New-AzureRmAutomationAccount cmdlet.</span></span>

## <span data-ttu-id="35a78-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="35a78-108">EXAMPLES</span></span>

### <span data-ttu-id="35a78-109">Пример 1: Настройка тегов для учетной записи автоматизации</span><span class="sxs-lookup"><span data-stu-id="35a78-109">Example 1: Set the tags for an Automation account</span></span>
```
PS C:\>$Tags = @{"tag01"="value01";"tag02"="value02"}
PS C:\> Set-AzureRmAutomationAccount -Name "AutomationAccount01" -ResourceGroupName "ResourceGroup01" -Tags $Tags
```

<span data-ttu-id="35a78-110">Первая команда присваивает переменной $Tags две пары "ключ-значение".</span><span class="sxs-lookup"><span data-stu-id="35a78-110">The first command assigns two key/value pairs to the $Tags variable.</span></span>
<span data-ttu-id="35a78-111">Вторая команда задает теги в $Tags для учетной записи автоматизации с именем AutomationAccount01.</span><span class="sxs-lookup"><span data-stu-id="35a78-111">The second command sets tags in $Tags for the Automation account named AutomationAccount01.</span></span>

### <span data-ttu-id="35a78-112">Пример 2: изменение плана для учетной записи автоматизации</span><span class="sxs-lookup"><span data-stu-id="35a78-112">Example 2: Change the plan for an Automation account</span></span>
```
PS C:\>Set-AzureRmAutomationAccount -Name "AutomationAccount01" -ResourceGroupName "ResourceGroup01" -Plan Basic
```

<span data-ttu-id="35a78-113">Эта команда изменяет план на Basic для учетной записи автоматизации с именем AutomationAccount01.</span><span class="sxs-lookup"><span data-stu-id="35a78-113">This command changes the plan to Basic for the Automation account named AutomationAccount01.</span></span>

## <span data-ttu-id="35a78-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="35a78-114">PARAMETERS</span></span>

### <span data-ttu-id="35a78-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="35a78-115">-DefaultProfile</span></span>
<span data-ttu-id="35a78-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="35a78-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="35a78-117">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="35a78-117">-Name</span></span>
<span data-ttu-id="35a78-118">Указывает имя учетной записи автоматизации, которую изменяет этот командлет.</span><span class="sxs-lookup"><span data-stu-id="35a78-118">Specifies the name of the Automation account that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="35a78-119">-Планирование</span><span class="sxs-lookup"><span data-stu-id="35a78-119">-Plan</span></span>
<span data-ttu-id="35a78-120">Указывает план для учетной записи автоматизации.</span><span class="sxs-lookup"><span data-stu-id="35a78-120">Specifies the plan for the Automation account.</span></span>
<span data-ttu-id="35a78-121">Допустимые значения:</span><span class="sxs-lookup"><span data-stu-id="35a78-121">Valid values are:</span></span>
- <span data-ttu-id="35a78-122">Базового</span><span class="sxs-lookup"><span data-stu-id="35a78-122">Basic</span></span>
- <span data-ttu-id="35a78-123">Бесплатно</span><span class="sxs-lookup"><span data-stu-id="35a78-123">Free</span></span>

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

### <span data-ttu-id="35a78-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="35a78-124">-ResourceGroupName</span></span>
<span data-ttu-id="35a78-125">Указывает имя группы ресурсов, которая содержит учетную запись автоматизации, которую изменяет этот командлет.</span><span class="sxs-lookup"><span data-stu-id="35a78-125">Specifies the name of a resource group that contains the Automation account that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="35a78-126">-Теги</span><span class="sxs-lookup"><span data-stu-id="35a78-126">-Tags</span></span>
<span data-ttu-id="35a78-127">Пары "ключ-значение" в виде хэш-таблицы.</span><span class="sxs-lookup"><span data-stu-id="35a78-127">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="35a78-128">Например: @ {Key0 = "value0"; key1 = $null; key2 = "значение2"}</span><span class="sxs-lookup"><span data-stu-id="35a78-128">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="35a78-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="35a78-129">CommonParameters</span></span>
<span data-ttu-id="35a78-130">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="35a78-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="35a78-131">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="35a78-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="35a78-132">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="35a78-132">INPUTS</span></span>

### <span data-ttu-id="35a78-133">System. String</span><span class="sxs-lookup"><span data-stu-id="35a78-133">System.String</span></span>

### <span data-ttu-id="35a78-134">System. Collections. IDictionary</span><span class="sxs-lookup"><span data-stu-id="35a78-134">System.Collections.IDictionary</span></span>

## <span data-ttu-id="35a78-135">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="35a78-135">OUTPUTS</span></span>

### <span data-ttu-id="35a78-136">Microsoft. Azure. Commands. Automation. Model. AutomationAccount</span><span class="sxs-lookup"><span data-stu-id="35a78-136">Microsoft.Azure.Commands.Automation.Model.AutomationAccount</span></span>

## <span data-ttu-id="35a78-137">Пуск</span><span class="sxs-lookup"><span data-stu-id="35a78-137">NOTES</span></span>

## <span data-ttu-id="35a78-138">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="35a78-138">RELATED LINKS</span></span>

[<span data-ttu-id="35a78-139">Get-AzureRmAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="35a78-139">Get-AzureRmAutomationAccount</span></span>](./Get-AzureRmAutomationAccount.md)

[<span data-ttu-id="35a78-140">New-AzureRmAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="35a78-140">New-AzureRmAutomationAccount</span></span>](./New-AzureRmAutomationAccount.md)

[<span data-ttu-id="35a78-141">Remove-AzureRmAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="35a78-141">Remove-AzureRmAutomationAccount</span></span>](./Remove-AzureRmAutomationAccount.md)
