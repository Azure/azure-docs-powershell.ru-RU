---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 2D5B16F0-0662-4D9F-A13F-808CE5EEBBA3
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/new-azautomationaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationAccount.md
ms.openlocfilehash: 350e1591081e1d171921a432a1b990066614c750
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94074978"
---
# <span data-ttu-id="679b2-101">New-AzAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="679b2-101">New-AzAutomationAccount</span></span>

## <span data-ttu-id="679b2-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="679b2-102">SYNOPSIS</span></span>
<span data-ttu-id="679b2-103">Создание учетной записи автоматизации.</span><span class="sxs-lookup"><span data-stu-id="679b2-103">Creates an Automation account.</span></span>

## <span data-ttu-id="679b2-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="679b2-104">SYNTAX</span></span>

```
New-AzAutomationAccount [-ResourceGroupName] <String> [-Name] <String> [-Location] <String> [-Plan <String>]
 [-Tags <IDictionary>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="679b2-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="679b2-105">DESCRIPTION</span></span>
<span data-ttu-id="679b2-106">Командлет **New-AzAutomationAccount** создает учетную запись службы автоматизации Azure в группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="679b2-106">The **New-AzAutomationAccount** cmdlet creates an Azure Automation account in a resource group.</span></span>
<span data-ttu-id="679b2-107">Учетная запись автоматизации является контейнером для ресурсов автоматизации, которые изолированы от ресурсов других учетных записей автоматизации.</span><span class="sxs-lookup"><span data-stu-id="679b2-107">An Automation account is a container for Automation resources that is isolated from the resources of other Automation accounts.</span></span> <span data-ttu-id="679b2-108">Ресурсы автоматизации включают Runbook, конфигурации необходимой конфигурации состояния (DSC), задания и ресурсы.</span><span class="sxs-lookup"><span data-stu-id="679b2-108">Automation resources include runbooks, Desired State Configuration (DSC) configurations, jobs, and assets.</span></span>

## <span data-ttu-id="679b2-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="679b2-109">EXAMPLES</span></span>

### <span data-ttu-id="679b2-110">Пример 1: создание учетной записи автоматизации</span><span class="sxs-lookup"><span data-stu-id="679b2-110">Example 1: Create an automation account</span></span>
```
PS C:\> New-AzAutomationAccount -Name "ContosoAutomationAccount" -Location "East US" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="679b2-111">Эта команда создает новую учетную запись автоматизации с именем ContosoAutomationAccount в регионе "Восток США".</span><span class="sxs-lookup"><span data-stu-id="679b2-111">This command creates a new automation account named ContosoAutomationAccount in the East US region.</span></span>

## <span data-ttu-id="679b2-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="679b2-112">PARAMETERS</span></span>

### <span data-ttu-id="679b2-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="679b2-113">-DefaultProfile</span></span>
<span data-ttu-id="679b2-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="679b2-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="679b2-115">-Location</span><span class="sxs-lookup"><span data-stu-id="679b2-115">-Location</span></span>
<span data-ttu-id="679b2-116">Указывает расположение, в котором этот командлет создает учетную запись автоматизации.</span><span class="sxs-lookup"><span data-stu-id="679b2-116">Specifies the location in which this cmdlet creates the Automation account.</span></span>
<span data-ttu-id="679b2-117">Для получения допустимых местоположений используйте командлет Get-AzLocation.</span><span class="sxs-lookup"><span data-stu-id="679b2-117">To obtain valid locations, use the Get-AzLocation cmdlet.</span></span>

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

### <span data-ttu-id="679b2-118">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="679b2-118">-Name</span></span>
<span data-ttu-id="679b2-119">Указывает имя учетной записи автоматизации.</span><span class="sxs-lookup"><span data-stu-id="679b2-119">Specifies a name for the Automation account.</span></span>

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

### <span data-ttu-id="679b2-120">-Планирование</span><span class="sxs-lookup"><span data-stu-id="679b2-120">-Plan</span></span>
<span data-ttu-id="679b2-121">Указывает план для учетной записи автоматизации.</span><span class="sxs-lookup"><span data-stu-id="679b2-121">Specifies the plan for the Automation account.</span></span>
<span data-ttu-id="679b2-122">Допустимые значения:</span><span class="sxs-lookup"><span data-stu-id="679b2-122">Valid values are:</span></span>
- <span data-ttu-id="679b2-123">Базового</span><span class="sxs-lookup"><span data-stu-id="679b2-123">Basic</span></span>
- <span data-ttu-id="679b2-124">Бесплатно</span><span class="sxs-lookup"><span data-stu-id="679b2-124">Free</span></span>

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

### <span data-ttu-id="679b2-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="679b2-125">-ResourceGroupName</span></span>
<span data-ttu-id="679b2-126">Указывает имя группы ресурсов, к которой этот командлет добавляет учетную запись автоматизации.</span><span class="sxs-lookup"><span data-stu-id="679b2-126">Specifies the name of a resource group to which this cmdlet adds an Automation account.</span></span>

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

### <span data-ttu-id="679b2-127">-Теги</span><span class="sxs-lookup"><span data-stu-id="679b2-127">-Tags</span></span>
<span data-ttu-id="679b2-128">Пары "ключ-значение" в виде хэш-таблицы.</span><span class="sxs-lookup"><span data-stu-id="679b2-128">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="679b2-129">Например: @ {Key0 = "value0"; key1 = $null; key2 = "значение2"}</span><span class="sxs-lookup"><span data-stu-id="679b2-129">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="679b2-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="679b2-130">CommonParameters</span></span>
<span data-ttu-id="679b2-131">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="679b2-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="679b2-132">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="679b2-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="679b2-133">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="679b2-133">INPUTS</span></span>

### <span data-ttu-id="679b2-134">System. String</span><span class="sxs-lookup"><span data-stu-id="679b2-134">System.String</span></span>

### <span data-ttu-id="679b2-135">System. Collections. IDictionary</span><span class="sxs-lookup"><span data-stu-id="679b2-135">System.Collections.IDictionary</span></span>

## <span data-ttu-id="679b2-136">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="679b2-136">OUTPUTS</span></span>

### <span data-ttu-id="679b2-137">Microsoft. Azure. Commands. Automation. Model. AutomationAccount</span><span class="sxs-lookup"><span data-stu-id="679b2-137">Microsoft.Azure.Commands.Automation.Model.AutomationAccount</span></span>

## <span data-ttu-id="679b2-138">Пуск</span><span class="sxs-lookup"><span data-stu-id="679b2-138">NOTES</span></span>

## <span data-ttu-id="679b2-139">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="679b2-139">RELATED LINKS</span></span>

[<span data-ttu-id="679b2-140">Get-AzAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="679b2-140">Get-AzAutomationAccount</span></span>](./Get-AzAutomationAccount.md)

[<span data-ttu-id="679b2-141">Remove-AzAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="679b2-141">Remove-AzAutomationAccount</span></span>](./Remove-AzAutomationAccount.md)

[<span data-ttu-id="679b2-142">Set-AzAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="679b2-142">Set-AzAutomationAccount</span></span>](./Set-AzAutomationAccount.md)
