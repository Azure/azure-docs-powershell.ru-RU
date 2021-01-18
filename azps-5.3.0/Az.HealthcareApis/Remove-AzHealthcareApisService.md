---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HealthcareApis.dll-Help.xml
Module Name: Az.HealthcareApis
online version: https://docs.microsoft.com/en-us/powershell/module/az.healthcareapis/remove-azhealthcareapisservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HealthcareApis/HealthcareApis/help/Remove-AzHealthcareApisService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HealthcareApis/HealthcareApis/help/Remove-AzHealthcareApisService.md
ms.openlocfilehash: 602ad3506f4a4fc0f8aa22128ca223e6a90f6ab5
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98504795"
---
# <span data-ttu-id="40568-101">Remove-AzHealthcareApisService</span><span class="sxs-lookup"><span data-stu-id="40568-101">Remove-AzHealthcareApisService</span></span>

## <span data-ttu-id="40568-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="40568-102">SYNOPSIS</span></span>
<span data-ttu-id="40568-103">Удаляет экземпляр службы.</span><span class="sxs-lookup"><span data-stu-id="40568-103">Deletes a service instance.</span></span>

## <span data-ttu-id="40568-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="40568-104">SYNTAX</span></span>

### <span data-ttu-id="40568-105">ServiceNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="40568-105">ServiceNameParameterSet (Default)</span></span>
```
Remove-AzHealthcareApisService -Name <String> -ResourceGroupName <String> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="40568-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="40568-106">InputObjectParameterSet</span></span>
```
Remove-AzHealthcareApisService -InputObject <PSHealthcareApisService> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="40568-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="40568-107">ResourceIdParameterSet</span></span>
```
Remove-AzHealthcareApisService [-ResourceId] <String> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="40568-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="40568-108">DESCRIPTION</span></span>
<span data-ttu-id="40568-109">Удаляет экземпляр службы.</span><span class="sxs-lookup"><span data-stu-id="40568-109">Deletes a service instance.</span></span>

## <span data-ttu-id="40568-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="40568-110">EXAMPLES</span></span>

### <span data-ttu-id="40568-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="40568-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzHealthcareApisService -Name MyService -ResourceGroupName MyResourceGroup
```

<span data-ttu-id="40568-112">Удаляет существующую службу HealthcareApis с предоставленным именем в предоставленной группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="40568-112">Deletes the existing HealthcareApis service with the provided name within a provided resource group.</span></span>

### <span data-ttu-id="40568-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="40568-113">Example 2</span></span>
```powershell
PS C:\> $ResourceId = "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/MyResourceGroup/providers/Microsoft.HealthcareApis/services/MyService
PS C:\> Remove-AzHealthcareApisService -ResourceId $ResourceId
```

<span data-ttu-id="40568-114">Удаляет существующую службу HealthcareApis с предоставленным ResourceId.</span><span class="sxs-lookup"><span data-stu-id="40568-114">Deletes the existing HealthcareApis service with the provided ResourceId.</span></span>

### <span data-ttu-id="40568-115">Пример 3</span><span class="sxs-lookup"><span data-stu-id="40568-115">Example 3</span></span>
```powershell
PS C:\> Get-AzHealthcareApisService -ResourceGroupName MyResourceGroup -Name MyService | Remove-AzHealthcareApisService
```

<span data-ttu-id="40568-116">Удаляет предоставленный объект службы HealthcareApis.</span><span class="sxs-lookup"><span data-stu-id="40568-116">Deletes the provided HealthcareApis service object.</span></span>

## <span data-ttu-id="40568-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="40568-117">PARAMETERS</span></span>

### <span data-ttu-id="40568-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="40568-118">-AsJob</span></span>
<span data-ttu-id="40568-119">Запуск cmdlet в качестве задания в фоновом режиме.</span><span class="sxs-lookup"><span data-stu-id="40568-119">Run cmdlet as a job in the background.</span></span>

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

### <span data-ttu-id="40568-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="40568-120">-DefaultProfile</span></span>
<span data-ttu-id="40568-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="40568-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="40568-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="40568-122">-InputObject</span></span>
<span data-ttu-id="40568-123">Объект службы HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="40568-123">HealthcareApis service object</span></span>

```yaml
Type: Microsoft.Azure.Commands.HealthcareApis.Models.PSHealthcareApisService
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="40568-124">-Name</span><span class="sxs-lookup"><span data-stu-id="40568-124">-Name</span></span>
<span data-ttu-id="40568-125">Имя службы HealthcareApis.</span><span class="sxs-lookup"><span data-stu-id="40568-125">HealthcareApis Service Name.</span></span>

```yaml
Type: System.String
Parameter Sets: ServiceNameParameterSet
Aliases: HealthcareApisName, FhirServiceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="40568-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="40568-126">-PassThru</span></span>
<span data-ttu-id="40568-127">Если он предоставлен, возвращается истина, если операция была успешной.</span><span class="sxs-lookup"><span data-stu-id="40568-127">If provided, returns true if the operation was successful</span></span>

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

### <span data-ttu-id="40568-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="40568-128">-ResourceGroupName</span></span>
<span data-ttu-id="40568-129">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="40568-129">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: ServiceNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="40568-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="40568-130">-ResourceId</span></span>
<span data-ttu-id="40568-131">HealthcareApis Service ResourceId.</span><span class="sxs-lookup"><span data-stu-id="40568-131">HealthcareApis Service ResourceId.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="40568-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="40568-132">-Confirm</span></span>
<span data-ttu-id="40568-133">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="40568-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="40568-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="40568-134">-WhatIf</span></span>
<span data-ttu-id="40568-135">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="40568-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="40568-136">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="40568-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="40568-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="40568-137">CommonParameters</span></span>
<span data-ttu-id="40568-138">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="40568-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="40568-139">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="40568-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="40568-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="40568-140">INPUTS</span></span>

### <span data-ttu-id="40568-141">Microsoft.Azure.Commands.HealthcareApis.Models.PSHealthcareApisService</span><span class="sxs-lookup"><span data-stu-id="40568-141">Microsoft.Azure.Commands.HealthcareApis.Models.PSHealthcareApisService</span></span>

### <span data-ttu-id="40568-142">System.String</span><span class="sxs-lookup"><span data-stu-id="40568-142">System.String</span></span>

## <span data-ttu-id="40568-143">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="40568-143">OUTPUTS</span></span>

### <span data-ttu-id="40568-144">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="40568-144">System.Boolean</span></span>

## <span data-ttu-id="40568-145">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="40568-145">NOTES</span></span>

## <span data-ttu-id="40568-146">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="40568-146">RELATED LINKS</span></span>
