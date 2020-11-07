---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-azmanagedapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzManagedApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzManagedApplication.md
ms.openlocfilehash: 8286bdd365f43881f09787dfb051e873d2fdeb9c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93905594"
---
# <span data-ttu-id="f055a-101">New-AzManagedApplication</span><span class="sxs-lookup"><span data-stu-id="f055a-101">New-AzManagedApplication</span></span>

## <span data-ttu-id="f055a-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="f055a-102">SYNOPSIS</span></span>
<span data-ttu-id="f055a-103">Создание приложения, управляемого Azure.</span><span class="sxs-lookup"><span data-stu-id="f055a-103">Creates an Azure managed application.</span></span>

## <span data-ttu-id="f055a-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="f055a-104">SYNTAX</span></span>

```
New-AzManagedApplication -Name <String> -ResourceGroupName <String> -ManagedResourceGroupName <String>
 [-ManagedApplicationDefinitionId <String>] -Location <String> [-Parameter <String>] -Kind <ApplicationKind>
 [-Plan <Hashtable>] [-Tag <Hashtable>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f055a-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f055a-105">DESCRIPTION</span></span>
<span data-ttu-id="f055a-106">Командлет **New-AzManagedApplication** создает управляемое приложение Azure.</span><span class="sxs-lookup"><span data-stu-id="f055a-106">The **New-AzManagedApplication** cmdlet creates an Azure Managed Application.</span></span>

## <span data-ttu-id="f055a-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="f055a-107">EXAMPLES</span></span>

### <span data-ttu-id="f055a-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="f055a-108">Example 1</span></span>
```
PS C:\>New-AzManagedApplication -Name "myManagedApplication" -ResourceGroupName myRG -ManagedResourceGroupName myManagedRG -ManagedApplicationDefinitionId "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myRG/providers/Microsoft.Solutions/applicationDefinitions/myAppDef" -Location eastus2euap -Kind ServiceCatalog
```

<span data-ttu-id="f055a-109">Эта команда создает управляемое приложение</span><span class="sxs-lookup"><span data-stu-id="f055a-109">This command creates a managed application</span></span>

## <span data-ttu-id="f055a-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="f055a-110">PARAMETERS</span></span>

### <span data-ttu-id="f055a-111">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="f055a-111">-ApiVersion</span></span>
<span data-ttu-id="f055a-112">Если этот параметр установлен, указывает версию используемого API поставщика ресурсов.</span><span class="sxs-lookup"><span data-stu-id="f055a-112">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="f055a-113">Если не указано, версия API автоматически определяется как самая свежая доступная.</span><span class="sxs-lookup"><span data-stu-id="f055a-113">If not specified, the API version is automatically determined as the latest available.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f055a-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f055a-114">-DefaultProfile</span></span>
<span data-ttu-id="f055a-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="f055a-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f055a-116">-Видах</span><span class="sxs-lookup"><span data-stu-id="f055a-116">-Kind</span></span>
<span data-ttu-id="f055a-117">Управляемое приложение.</span><span class="sxs-lookup"><span data-stu-id="f055a-117">The managed application kind.</span></span>
<span data-ttu-id="f055a-118">Один из решений Marketplace или servicecatalog</span><span class="sxs-lookup"><span data-stu-id="f055a-118">One of marketplace or servicecatalog</span></span>

```yaml
Type: Microsoft.Azure.Commands.ResourceManager.Cmdlets.Entities.Application.ApplicationKind
Parameter Sets: (All)
Aliases:
Accepted values: ServiceCatalog, MarketPlace

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f055a-119">-Location</span><span class="sxs-lookup"><span data-stu-id="f055a-119">-Location</span></span>
<span data-ttu-id="f055a-120">Расположение ресурса.</span><span class="sxs-lookup"><span data-stu-id="f055a-120">The resource location.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f055a-121">-ManagedApplicationDefinitionId</span><span class="sxs-lookup"><span data-stu-id="f055a-121">-ManagedApplicationDefinitionId</span></span>
<span data-ttu-id="f055a-122">Имя управляемой группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="f055a-122">The managed resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f055a-123">-ManagedResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f055a-123">-ManagedResourceGroupName</span></span>
<span data-ttu-id="f055a-124">Имя управляемой группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="f055a-124">The managed resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f055a-125">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="f055a-125">-Name</span></span>
<span data-ttu-id="f055a-126">Имя управляемого приложения.</span><span class="sxs-lookup"><span data-stu-id="f055a-126">The managed application name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f055a-127">-Параметр</span><span class="sxs-lookup"><span data-stu-id="f055a-127">-Parameter</span></span>
<span data-ttu-id="f055a-128">Форматированная строка JSON параметров управляемого приложения.</span><span class="sxs-lookup"><span data-stu-id="f055a-128">The JSON formatted string of parameters for managed application.</span></span>
<span data-ttu-id="f055a-129">Это может быть путь к имени файла или универсальному коду ресурса (URI), содержащему параметры, или параметрам в виде строки.</span><span class="sxs-lookup"><span data-stu-id="f055a-129">This can either be a path to a file name or uri containing the parameters, or the parameters as string.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f055a-130">-Планирование</span><span class="sxs-lookup"><span data-stu-id="f055a-130">-Plan</span></span>
<span data-ttu-id="f055a-131">Хэш-таблица, представляющая свойства плана управляемых приложений.</span><span class="sxs-lookup"><span data-stu-id="f055a-131">A hash table which represents managed application plan properties.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: PlanObject

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f055a-132">-Pre</span><span class="sxs-lookup"><span data-stu-id="f055a-132">-Pre</span></span>
<span data-ttu-id="f055a-133">Если этот параметр установлен, при автоматическом определении версии для использования командлета необходимо использовать предварительно выпущенные версии API.</span><span class="sxs-lookup"><span data-stu-id="f055a-133">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f055a-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f055a-134">-ResourceGroupName</span></span>
<span data-ttu-id="f055a-135">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="f055a-135">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f055a-136">-Тег</span><span class="sxs-lookup"><span data-stu-id="f055a-136">-Tag</span></span>
<span data-ttu-id="f055a-137">Хэш-таблица, представляющая Теги ресурсов.</span><span class="sxs-lookup"><span data-stu-id="f055a-137">A hashtable which represents resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f055a-138">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f055a-138">-Confirm</span></span>
<span data-ttu-id="f055a-139">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="f055a-139">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f055a-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f055a-140">-WhatIf</span></span>
<span data-ttu-id="f055a-141">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="f055a-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f055a-142">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="f055a-142">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f055a-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f055a-143">CommonParameters</span></span>
<span data-ttu-id="f055a-144">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="f055a-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f055a-145">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f055a-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f055a-146">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="f055a-146">INPUTS</span></span>

### <span data-ttu-id="f055a-147">System. String</span><span class="sxs-lookup"><span data-stu-id="f055a-147">System.String</span></span>

### <span data-ttu-id="f055a-148">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="f055a-148">System.Collections.Hashtable</span></span>

## <span data-ttu-id="f055a-149">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="f055a-149">OUTPUTS</span></span>

### <span data-ttu-id="f055a-150">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="f055a-150">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="f055a-151">Пуск</span><span class="sxs-lookup"><span data-stu-id="f055a-151">NOTES</span></span>

## <span data-ttu-id="f055a-152">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f055a-152">RELATED LINKS</span></span>
