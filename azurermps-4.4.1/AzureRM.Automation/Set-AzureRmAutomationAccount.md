---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: B1897EFC-0184-4A8B-B8E4-203CC8E3B179
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Set-AzureRmAutomationAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Set-AzureRmAutomationAccount.md
ms.openlocfilehash: 8ad63c37c366c0f9c7693585f3a3c2fd57de4fdd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93560548"
---
# <span data-ttu-id="8f189-101">Set-AzureRmAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="8f189-101">Set-AzureRmAutomationAccount</span></span>

## <span data-ttu-id="8f189-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="8f189-102">SYNOPSIS</span></span>
<span data-ttu-id="8f189-103">Изменение учетной записи автоматизации.</span><span class="sxs-lookup"><span data-stu-id="8f189-103">Modifies an Automation account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8f189-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="8f189-104">SYNTAX</span></span>

```
Set-AzureRmAutomationAccount [-ResourceGroupName] <String> [-Name] <String> [-Plan <String>]
 [-Tags <IDictionary>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8f189-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="8f189-105">DESCRIPTION</span></span>
<span data-ttu-id="8f189-106">Командлет **Set-AzureRmAutomationAccount** изменяет учетную запись службы автоматизации Azure.</span><span class="sxs-lookup"><span data-stu-id="8f189-106">The **Set-AzureRmAutomationAccount** cmdlet modifies an Azure Automation account.</span></span>

<span data-ttu-id="8f189-107">Дополнительные сведения об учетных записях автоматизации можно найти в командлете New-AzureRmAutomationAccount.</span><span class="sxs-lookup"><span data-stu-id="8f189-107">For more information about Automation accounts, see the New-AzureRmAutomationAccount cmdlet.</span></span>

## <span data-ttu-id="8f189-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="8f189-108">EXAMPLES</span></span>

### <span data-ttu-id="8f189-109">Пример 1: Настройка тегов для учетной записи автоматизации</span><span class="sxs-lookup"><span data-stu-id="8f189-109">Example 1: Set the tags for an Automation account</span></span>
```
PS C:\>$Tags = @{"tag01"="value01";"tag02"="value02"}
PS C:\> Set-AzureRmAutomationAccount -Name "AutomationAccount01" -ResourceGroupName "ResourceGroup01" -Tags $Tags
```

<span data-ttu-id="8f189-110">Первая команда присваивает переменной $Tags две пары "ключ-значение".</span><span class="sxs-lookup"><span data-stu-id="8f189-110">The first command assigns two key/value pairs to the $Tags variable.</span></span>

<span data-ttu-id="8f189-111">Вторая команда задает теги в $Tags для учетной записи автоматизации с именем AutomationAccount01.</span><span class="sxs-lookup"><span data-stu-id="8f189-111">The second command sets tags in $Tags for the Automation account named AutomationAccount01.</span></span>

### <span data-ttu-id="8f189-112">Пример 2: изменение плана для учетной записи автоматизации</span><span class="sxs-lookup"><span data-stu-id="8f189-112">Example 2: Change the plan for an Automation account</span></span>
```
PS C:\>Set-AzureRmAutomationAccount -Name "AutomationAccount01" -ResourceGroupName "ResourceGroup01" -Plan Basic
```

<span data-ttu-id="8f189-113">Эта команда изменяет план на Basic для учетной записи автоматизации с именем AutomationAccount01.</span><span class="sxs-lookup"><span data-stu-id="8f189-113">This command changes the plan to Basic for the Automation account named AutomationAccount01.</span></span>

## <span data-ttu-id="8f189-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="8f189-114">PARAMETERS</span></span>

### <span data-ttu-id="8f189-115">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="8f189-115">-Name</span></span>
<span data-ttu-id="8f189-116">Указывает имя учетной записи автоматизации, которую изменяет этот командлет.</span><span class="sxs-lookup"><span data-stu-id="8f189-116">Specifies the name of the Automation account that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="8f189-117">-Планирование</span><span class="sxs-lookup"><span data-stu-id="8f189-117">-Plan</span></span>
<span data-ttu-id="8f189-118">Указывает план для учетной записи автоматизации.</span><span class="sxs-lookup"><span data-stu-id="8f189-118">Specifies the plan for the Automation account.</span></span>
<span data-ttu-id="8f189-119">Допустимые значения:</span><span class="sxs-lookup"><span data-stu-id="8f189-119">Valid values are:</span></span>

- <span data-ttu-id="8f189-120">Базового</span><span class="sxs-lookup"><span data-stu-id="8f189-120">Basic</span></span>
- <span data-ttu-id="8f189-121">Бесплатно</span><span class="sxs-lookup"><span data-stu-id="8f189-121">Free</span></span>

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

### <span data-ttu-id="8f189-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8f189-122">-ResourceGroupName</span></span>
<span data-ttu-id="8f189-123">Указывает имя группы ресурсов, которая содержит учетную запись автоматизации, которую изменяет этот командлет.</span><span class="sxs-lookup"><span data-stu-id="8f189-123">Specifies the name of a resource group that contains the Automation account that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="8f189-124">-Теги</span><span class="sxs-lookup"><span data-stu-id="8f189-124">-Tags</span></span>
<span data-ttu-id="8f189-125">Пары "ключ-значение" в виде хэш-таблицы.</span><span class="sxs-lookup"><span data-stu-id="8f189-125">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="8f189-126">Например:</span><span class="sxs-lookup"><span data-stu-id="8f189-126">For example:</span></span>

<span data-ttu-id="8f189-127">@ {Key0 = "value0"; key1 = $null; key2 = "значение2"}</span><span class="sxs-lookup"><span data-stu-id="8f189-127">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="8f189-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8f189-128">-DefaultProfile</span></span>
<span data-ttu-id="8f189-129">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="8f189-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8f189-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8f189-130">CommonParameters</span></span>
<span data-ttu-id="8f189-131">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="8f189-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8f189-132">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8f189-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8f189-133">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="8f189-133">INPUTS</span></span>

## <span data-ttu-id="8f189-134">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="8f189-134">OUTPUTS</span></span>

### <span data-ttu-id="8f189-135">Microsoft. Azure. Commands. Automation. Model. AutomationAccount</span><span class="sxs-lookup"><span data-stu-id="8f189-135">Microsoft.Azure.Commands.Automation.Model.AutomationAccount</span></span>

## <span data-ttu-id="8f189-136">Пуск</span><span class="sxs-lookup"><span data-stu-id="8f189-136">NOTES</span></span>

## <span data-ttu-id="8f189-137">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="8f189-137">RELATED LINKS</span></span>

[<span data-ttu-id="8f189-138">Get-AzureRmAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="8f189-138">Get-AzureRmAutomationAccount</span></span>](./Get-AzureRmAutomationAccount.md)

[<span data-ttu-id="8f189-139">New-AzureRmAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="8f189-139">New-AzureRmAutomationAccount</span></span>](./New-AzureRmAutomationAccount.md)

[<span data-ttu-id="8f189-140">Remove-AzureRmAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="8f189-140">Remove-AzureRmAutomationAccount</span></span>](./Remove-AzureRmAutomationAccount.md)
