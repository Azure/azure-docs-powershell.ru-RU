---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 2D5B16F0-0662-4D9F-A13F-808CE5EEBBA3
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/new-azurermautomationaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/New-AzureRmAutomationAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/New-AzureRmAutomationAccount.md
ms.openlocfilehash: c82a68e7859945b1fdb91f6d44a1ebbcef6d2cff
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93559368"
---
# <span data-ttu-id="8f108-101">New-AzureRmAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="8f108-101">New-AzureRmAutomationAccount</span></span>

## <span data-ttu-id="8f108-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="8f108-102">SYNOPSIS</span></span>
<span data-ttu-id="8f108-103">Создание учетной записи автоматизации.</span><span class="sxs-lookup"><span data-stu-id="8f108-103">Creates an Automation account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8f108-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="8f108-104">SYNTAX</span></span>

```
New-AzureRmAutomationAccount [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [-Plan <String>] [-Tags <IDictionary>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8f108-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="8f108-105">DESCRIPTION</span></span>
<span data-ttu-id="8f108-106">Командлет **New-AzureRmAutomationAccount** создает учетную запись службы автоматизации Azure в группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="8f108-106">The **New-AzureRmAutomationAccount** cmdlet creates an Azure Automation account in a resource group.</span></span>

<span data-ttu-id="8f108-107">Учетная запись автоматизации является контейнером для ресурсов автоматизации, которые изолированы от ресурсов других учетных записей автоматизации.</span><span class="sxs-lookup"><span data-stu-id="8f108-107">An Automation account is a container for Automation resources that is isolated from the resources of other Automation accounts.</span></span> <span data-ttu-id="8f108-108">Ресурсы автоматизации включают Runbook, конфигурации необходимой конфигурации состояния (DSC), задания и ресурсы.</span><span class="sxs-lookup"><span data-stu-id="8f108-108">Automation resources include runbooks, Desired State Configuration (DSC) configurations, jobs, and assets.</span></span>

## <span data-ttu-id="8f108-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="8f108-109">EXAMPLES</span></span>

### <span data-ttu-id="8f108-110">Пример 1: создание учетной записи автоматизации</span><span class="sxs-lookup"><span data-stu-id="8f108-110">Example 1: Create an automation account</span></span>
```
PS C:\> New-AzureRmAutomationAccount -Name "ContosoAutomationAccount" -Location "East US" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="8f108-111">Эта команда создает новую учетную запись автоматизации с именем ContosoAutomationAccount в регионе "Восток США".</span><span class="sxs-lookup"><span data-stu-id="8f108-111">This command creates a new automation account named ContosoAutomationAccount in the East US region.</span></span>

## <span data-ttu-id="8f108-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="8f108-112">PARAMETERS</span></span>

### <span data-ttu-id="8f108-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8f108-113">-DefaultProfile</span></span>
<span data-ttu-id="8f108-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="8f108-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8f108-115">-Location</span><span class="sxs-lookup"><span data-stu-id="8f108-115">-Location</span></span>
<span data-ttu-id="8f108-116">Указывает расположение, в котором этот командлет создает учетную запись автоматизации.</span><span class="sxs-lookup"><span data-stu-id="8f108-116">Specifies the location in which this cmdlet creates the Automation account.</span></span>
<span data-ttu-id="8f108-117">Для получения допустимых местоположений используйте командлет Get-AzureRMLocation.</span><span class="sxs-lookup"><span data-stu-id="8f108-117">To obtain valid locations, use the Get-AzureRMLocation cmdlet.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8f108-118">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="8f108-118">-Name</span></span>
<span data-ttu-id="8f108-119">Указывает имя учетной записи автоматизации.</span><span class="sxs-lookup"><span data-stu-id="8f108-119">Specifies a name for the Automation account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: AutomationAccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8f108-120">-Планирование</span><span class="sxs-lookup"><span data-stu-id="8f108-120">-Plan</span></span>
<span data-ttu-id="8f108-121">Указывает план для учетной записи автоматизации.</span><span class="sxs-lookup"><span data-stu-id="8f108-121">Specifies the plan for the Automation account.</span></span>
<span data-ttu-id="8f108-122">Допустимые значения:</span><span class="sxs-lookup"><span data-stu-id="8f108-122">Valid values are:</span></span>

- <span data-ttu-id="8f108-123">Базового</span><span class="sxs-lookup"><span data-stu-id="8f108-123">Basic</span></span>
- <span data-ttu-id="8f108-124">Бесплатно</span><span class="sxs-lookup"><span data-stu-id="8f108-124">Free</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Free, Basic

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8f108-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8f108-125">-ResourceGroupName</span></span>
<span data-ttu-id="8f108-126">Указывает имя группы ресурсов, к которой этот командлет добавляет учетную запись автоматизации.</span><span class="sxs-lookup"><span data-stu-id="8f108-126">Specifies the name of a resource group to which this cmdlet adds an Automation account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8f108-127">-Теги</span><span class="sxs-lookup"><span data-stu-id="8f108-127">-Tags</span></span>
<span data-ttu-id="8f108-128">Пары "ключ-значение" в виде хэш-таблицы.</span><span class="sxs-lookup"><span data-stu-id="8f108-128">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="8f108-129">Например:</span><span class="sxs-lookup"><span data-stu-id="8f108-129">For example:</span></span>

<span data-ttu-id="8f108-130">@ {Key0 = "value0"; key1 = $null; key2 = "значение2"}</span><span class="sxs-lookup"><span data-stu-id="8f108-130">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: IDictionary
Parameter Sets: (All)
Aliases: Tag

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8f108-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8f108-131">CommonParameters</span></span>
<span data-ttu-id="8f108-132">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="8f108-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8f108-133">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8f108-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8f108-134">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="8f108-134">INPUTS</span></span>

### <span data-ttu-id="8f108-135">Ничего</span><span class="sxs-lookup"><span data-stu-id="8f108-135">None</span></span>
<span data-ttu-id="8f108-136">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="8f108-136">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="8f108-137">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="8f108-137">OUTPUTS</span></span>

### <span data-ttu-id="8f108-138">Microsoft. Azure. Commands. Automation. Model. AutomationAccount</span><span class="sxs-lookup"><span data-stu-id="8f108-138">Microsoft.Azure.Commands.Automation.Model.AutomationAccount</span></span>

## <span data-ttu-id="8f108-139">Пуск</span><span class="sxs-lookup"><span data-stu-id="8f108-139">NOTES</span></span>

## <span data-ttu-id="8f108-140">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="8f108-140">RELATED LINKS</span></span>

[<span data-ttu-id="8f108-141">Get-AzureRmAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="8f108-141">Get-AzureRmAutomationAccount</span></span>](./Get-AzureRmAutomationAccount.md)

[<span data-ttu-id="8f108-142">Remove-AzureRmAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="8f108-142">Remove-AzureRmAutomationAccount</span></span>](./Remove-AzureRmAutomationAccount.md)

[<span data-ttu-id="8f108-143">Set-AzureRmAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="8f108-143">Set-AzureRmAutomationAccount</span></span>](./Set-AzureRmAutomationAccount.md)
