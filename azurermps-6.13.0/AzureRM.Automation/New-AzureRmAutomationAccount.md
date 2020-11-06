---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 2D5B16F0-0662-4D9F-A13F-808CE5EEBBA3
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/new-azurermautomationaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/New-AzureRmAutomationAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/New-AzureRmAutomationAccount.md
ms.openlocfilehash: 2d7c038f9f226f074bfe534df40471959607f3d6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93556868"
---
# <span data-ttu-id="34129-101">New-AzureRmAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="34129-101">New-AzureRmAutomationAccount</span></span>

## <span data-ttu-id="34129-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="34129-102">SYNOPSIS</span></span>
<span data-ttu-id="34129-103">Создание учетной записи автоматизации.</span><span class="sxs-lookup"><span data-stu-id="34129-103">Creates an Automation account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="34129-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="34129-104">SYNTAX</span></span>

```
New-AzureRmAutomationAccount [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [-Plan <String>] [-Tags <IDictionary>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="34129-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="34129-105">DESCRIPTION</span></span>
<span data-ttu-id="34129-106">Командлет **New-AzureRmAutomationAccount** создает учетную запись службы автоматизации Azure в группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="34129-106">The **New-AzureRmAutomationAccount** cmdlet creates an Azure Automation account in a resource group.</span></span>
<span data-ttu-id="34129-107">Учетная запись автоматизации является контейнером для ресурсов автоматизации, которые изолированы от ресурсов других учетных записей автоматизации.</span><span class="sxs-lookup"><span data-stu-id="34129-107">An Automation account is a container for Automation resources that is isolated from the resources of other Automation accounts.</span></span> <span data-ttu-id="34129-108">Ресурсы автоматизации включают Runbook, конфигурации необходимой конфигурации состояния (DSC), задания и ресурсы.</span><span class="sxs-lookup"><span data-stu-id="34129-108">Automation resources include runbooks, Desired State Configuration (DSC) configurations, jobs, and assets.</span></span>

## <span data-ttu-id="34129-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="34129-109">EXAMPLES</span></span>

### <span data-ttu-id="34129-110">Пример 1: создание учетной записи автоматизации</span><span class="sxs-lookup"><span data-stu-id="34129-110">Example 1: Create an automation account</span></span>
```
PS C:\> New-AzureRmAutomationAccount -Name "ContosoAutomationAccount" -Location "East US" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="34129-111">Эта команда создает новую учетную запись автоматизации с именем ContosoAutomationAccount в регионе "Восток США".</span><span class="sxs-lookup"><span data-stu-id="34129-111">This command creates a new automation account named ContosoAutomationAccount in the East US region.</span></span>

## <span data-ttu-id="34129-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="34129-112">PARAMETERS</span></span>

### <span data-ttu-id="34129-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="34129-113">-DefaultProfile</span></span>
<span data-ttu-id="34129-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="34129-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="34129-115">-Location</span><span class="sxs-lookup"><span data-stu-id="34129-115">-Location</span></span>
<span data-ttu-id="34129-116">Указывает расположение, в котором этот командлет создает учетную запись автоматизации.</span><span class="sxs-lookup"><span data-stu-id="34129-116">Specifies the location in which this cmdlet creates the Automation account.</span></span>
<span data-ttu-id="34129-117">Для получения допустимых местоположений используйте командлет Get-AzureRMLocation.</span><span class="sxs-lookup"><span data-stu-id="34129-117">To obtain valid locations, use the Get-AzureRMLocation cmdlet.</span></span>

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

### <span data-ttu-id="34129-118">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="34129-118">-Name</span></span>
<span data-ttu-id="34129-119">Указывает имя учетной записи автоматизации.</span><span class="sxs-lookup"><span data-stu-id="34129-119">Specifies a name for the Automation account.</span></span>

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

### <span data-ttu-id="34129-120">-Планирование</span><span class="sxs-lookup"><span data-stu-id="34129-120">-Plan</span></span>
<span data-ttu-id="34129-121">Указывает план для учетной записи автоматизации.</span><span class="sxs-lookup"><span data-stu-id="34129-121">Specifies the plan for the Automation account.</span></span>
<span data-ttu-id="34129-122">Допустимые значения:</span><span class="sxs-lookup"><span data-stu-id="34129-122">Valid values are:</span></span>
- <span data-ttu-id="34129-123">Базового</span><span class="sxs-lookup"><span data-stu-id="34129-123">Basic</span></span>
- <span data-ttu-id="34129-124">Бесплатно</span><span class="sxs-lookup"><span data-stu-id="34129-124">Free</span></span>

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

### <span data-ttu-id="34129-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="34129-125">-ResourceGroupName</span></span>
<span data-ttu-id="34129-126">Указывает имя группы ресурсов, к которой этот командлет добавляет учетную запись автоматизации.</span><span class="sxs-lookup"><span data-stu-id="34129-126">Specifies the name of a resource group to which this cmdlet adds an Automation account.</span></span>

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

### <span data-ttu-id="34129-127">-Теги</span><span class="sxs-lookup"><span data-stu-id="34129-127">-Tags</span></span>
<span data-ttu-id="34129-128">Пары "ключ-значение" в виде хэш-таблицы.</span><span class="sxs-lookup"><span data-stu-id="34129-128">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="34129-129">Например: @ {Key0 = "value0"; key1 = $null; key2 = "значение2"}</span><span class="sxs-lookup"><span data-stu-id="34129-129">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="34129-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="34129-130">CommonParameters</span></span>
<span data-ttu-id="34129-131">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="34129-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="34129-132">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="34129-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="34129-133">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="34129-133">INPUTS</span></span>

### <span data-ttu-id="34129-134">System. String</span><span class="sxs-lookup"><span data-stu-id="34129-134">System.String</span></span>

### <span data-ttu-id="34129-135">System. Collections. IDictionary</span><span class="sxs-lookup"><span data-stu-id="34129-135">System.Collections.IDictionary</span></span>

## <span data-ttu-id="34129-136">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="34129-136">OUTPUTS</span></span>

### <span data-ttu-id="34129-137">Microsoft. Azure. Commands. Automation. Model. AutomationAccount</span><span class="sxs-lookup"><span data-stu-id="34129-137">Microsoft.Azure.Commands.Automation.Model.AutomationAccount</span></span>

## <span data-ttu-id="34129-138">Пуск</span><span class="sxs-lookup"><span data-stu-id="34129-138">NOTES</span></span>

## <span data-ttu-id="34129-139">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="34129-139">RELATED LINKS</span></span>

[<span data-ttu-id="34129-140">Get-AzureRmAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="34129-140">Get-AzureRmAutomationAccount</span></span>](./Get-AzureRmAutomationAccount.md)

[<span data-ttu-id="34129-141">Remove-AzureRmAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="34129-141">Remove-AzureRmAutomationAccount</span></span>](./Remove-AzureRmAutomationAccount.md)

[<span data-ttu-id="34129-142">Set-AzureRmAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="34129-142">Set-AzureRmAutomationAccount</span></span>](./Set-AzureRmAutomationAccount.md)
