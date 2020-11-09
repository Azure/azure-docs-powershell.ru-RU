---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/export-aztemplatespec
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Export-AzTemplateSpec.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Export-AzTemplateSpec.md
ms.openlocfilehash: 9b0db1cc72064b502b9961fba73598b94790af1a
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94316063"
---
# <span data-ttu-id="eca8a-101">Export-AzTemplateSpec</span><span class="sxs-lookup"><span data-stu-id="eca8a-101">Export-AzTemplateSpec</span></span>

## <span data-ttu-id="eca8a-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="eca8a-102">SYNOPSIS</span></span>
<span data-ttu-id="eca8a-103">Экспортирует спецификацию шаблона в локальную файловую систему</span><span class="sxs-lookup"><span data-stu-id="eca8a-103">Exports a Template Spec to the local filesystem</span></span>

## <span data-ttu-id="eca8a-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="eca8a-104">SYNTAX</span></span>

### <span data-ttu-id="eca8a-105">ExportByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="eca8a-105">ExportByNameParameterSet (Default)</span></span>
```
Export-AzTemplateSpec [-ResourceGroupName] <String> [-Name] <String> -Version <String> -OutputFolder <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="eca8a-106">ExportByIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="eca8a-106">ExportByIdParameterSet</span></span>
```
Export-AzTemplateSpec [-ResourceId] <String> -Version <String> -OutputFolder <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="eca8a-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="eca8a-107">DESCRIPTION</span></span>
<span data-ttu-id="eca8a-108">Экспортирует определенную спецификацию шаблона в локальную файловую систему.</span><span class="sxs-lookup"><span data-stu-id="eca8a-108">Exports a specific Template Spec version to the local filesystem.</span></span>

## <span data-ttu-id="eca8a-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="eca8a-109">EXAMPLES</span></span>

### <span data-ttu-id="eca8a-110">Пример 1: экспорт по имени</span><span class="sxs-lookup"><span data-stu-id="eca8a-110">Example 1: Export by name</span></span>
```powershell
PS C:\> Export-AzTemplateSpec -ResourceGroupName 'myRG' -Name 'MyTemplateSpec' -Version 'v1.0' -OutputFolder 'v1'
```

<span data-ttu-id="eca8a-111">Экспортирует версию v 1.0 спецификации шаблона с именем "MyTemplateSpec" в группе ресурсов "myRG" в локальную папку выходных данных "v1".</span><span class="sxs-lookup"><span data-stu-id="eca8a-111">Exports version 'v1.0' of the Template Spec named 'MyTemplateSpec' within the resource group 'myRG' to the local output folder "v1".</span></span>

### <span data-ttu-id="eca8a-112">Пример 2: экспорт по идентификатору ресурса</span><span class="sxs-lookup"><span data-stu-id="eca8a-112">Example 2: Export by resource id</span></span>
```powershell
PS C:\> Export-AzTemplateSpec -ResourceId '/subscriptions/{subId}/resourceGroups/myRG/providers/Microsoft.Resources/templateSpecs/MyTemplateSpec' -Version 'v1.0' -OutputFolder 'v1'
```

<span data-ttu-id="eca8a-113">Экспортирует версию версии 1.0 спецификации шаблона с именем "MyTemplateSpec" в группе ресурсов "myRG" для подписки \{ subId \} в локальную папку выходных данных "v1".</span><span class="sxs-lookup"><span data-stu-id="eca8a-113">Exports version 'v1.0' of the Template Spec named 'MyTemplateSpec' within the resource group 'myRG' of subscription \{subId\} to the local output folder "v1".</span></span>

## <span data-ttu-id="eca8a-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="eca8a-114">PARAMETERS</span></span>

### <span data-ttu-id="eca8a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eca8a-115">-DefaultProfile</span></span>
<span data-ttu-id="eca8a-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="eca8a-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="eca8a-117">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="eca8a-117">-Name</span></span>
<span data-ttu-id="eca8a-118">Название спецификации шаблона.</span><span class="sxs-lookup"><span data-stu-id="eca8a-118">The name of the template spec.</span></span>

```yaml
Type: System.String
Parameter Sets: ExportByNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eca8a-119">-OutputFolder</span><span class="sxs-lookup"><span data-stu-id="eca8a-119">-OutputFolder</span></span>
<span data-ttu-id="eca8a-120">Путь к папке, в которой будет выводиться версия спецификации шаблона.</span><span class="sxs-lookup"><span data-stu-id="eca8a-120">The path to the folder where the template spec version will be output to.</span></span>

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

### <span data-ttu-id="eca8a-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eca8a-121">-ResourceGroupName</span></span>
<span data-ttu-id="eca8a-122">Имя группы ресурсов для спецификации шаблона.</span><span class="sxs-lookup"><span data-stu-id="eca8a-122">The name of the template spec's resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: ExportByNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eca8a-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="eca8a-123">-ResourceId</span></span>
<span data-ttu-id="eca8a-124">Полный идентификатор ресурса спецификации шаблона. Пример:/subscriptions/{subId}/resourceGroups/{rgName}/providers/Microsoft.Resources/templateSpecs/{templateSpecName}</span><span class="sxs-lookup"><span data-stu-id="eca8a-124">The fully qualified resource Id of the template spec. Example: /subscriptions/{subId}/resourceGroups/{rgName}/providers/Microsoft.Resources/templateSpecs/{templateSpecName}</span></span>

```yaml
Type: System.String
Parameter Sets: ExportByIdParameterSet
Aliases: Id

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eca8a-125">-Version</span><span class="sxs-lookup"><span data-stu-id="eca8a-125">-Version</span></span>
<span data-ttu-id="eca8a-126">Версия спецификации шаблона для экспорта.</span><span class="sxs-lookup"><span data-stu-id="eca8a-126">The version of the template spec to export.</span></span>

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

### <span data-ttu-id="eca8a-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="eca8a-127">-Confirm</span></span>
<span data-ttu-id="eca8a-128">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="eca8a-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="eca8a-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="eca8a-129">-WhatIf</span></span>
<span data-ttu-id="eca8a-130">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="eca8a-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="eca8a-131">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="eca8a-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="eca8a-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eca8a-132">CommonParameters</span></span>
<span data-ttu-id="eca8a-133">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="eca8a-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eca8a-134">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="eca8a-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eca8a-135">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="eca8a-135">INPUTS</span></span>

### <span data-ttu-id="eca8a-136">System. String</span><span class="sxs-lookup"><span data-stu-id="eca8a-136">System.String</span></span>

## <span data-ttu-id="eca8a-137">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="eca8a-137">OUTPUTS</span></span>

### <span data-ttu-id="eca8a-138">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="eca8a-138">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="eca8a-139">Пуск</span><span class="sxs-lookup"><span data-stu-id="eca8a-139">NOTES</span></span>

## <span data-ttu-id="eca8a-140">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="eca8a-140">RELATED LINKS</span></span>
