---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HealthcareApis.dll-Help.xml
Module Name: Az.HealthcareApis
online version: https://docs.microsoft.com/en-us/powershell/module/az.healthcareapis/remove-azhealthcareapisservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HealthcareApis/HealthcareApis/help/Remove-AzHealthcareApisService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HealthcareApis/HealthcareApis/help/Remove-AzHealthcareApisService.md
ms.openlocfilehash: 12db158089473c5f0cfb01e24b762ecf192f8991
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94243375"
---
# <span data-ttu-id="ad6bf-101">Remove-AzHealthcareApisService</span><span class="sxs-lookup"><span data-stu-id="ad6bf-101">Remove-AzHealthcareApisService</span></span>

## <span data-ttu-id="ad6bf-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="ad6bf-102">SYNOPSIS</span></span>
<span data-ttu-id="ad6bf-103">Удаляет экземпляр службы.</span><span class="sxs-lookup"><span data-stu-id="ad6bf-103">Deletes a service instance.</span></span>

## <span data-ttu-id="ad6bf-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="ad6bf-104">SYNTAX</span></span>

### <span data-ttu-id="ad6bf-105">ServiceNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="ad6bf-105">ServiceNameParameterSet (Default)</span></span>
```
Remove-AzHealthcareApisService -Name <String> -ResourceGroupName <String> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ad6bf-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ad6bf-106">InputObjectParameterSet</span></span>
```
Remove-AzHealthcareApisService -InputObject <PSHealthcareApisService> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ad6bf-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ad6bf-107">ResourceIdParameterSet</span></span>
```
Remove-AzHealthcareApisService [-ResourceId] <String> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ad6bf-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ad6bf-108">DESCRIPTION</span></span>
<span data-ttu-id="ad6bf-109">Удаляет экземпляр службы.</span><span class="sxs-lookup"><span data-stu-id="ad6bf-109">Deletes a service instance.</span></span>

## <span data-ttu-id="ad6bf-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="ad6bf-110">EXAMPLES</span></span>

### <span data-ttu-id="ad6bf-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="ad6bf-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzHealthcareApisService -Name MyService -ResourceGroupName MyResourceGroup
```

<span data-ttu-id="ad6bf-112">Удаляет существующую службу HealthcareApis с указанным именем в указанной группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="ad6bf-112">Deletes the existing HealthcareApis service with the provided name within a provided resource group.</span></span>

### <span data-ttu-id="ad6bf-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="ad6bf-113">Example 2</span></span>
```powershell
PS C:\> $ResourceId = "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/MyResourceGroup/providers/Microsoft.HealthcareApis/services/MyService
PS C:\> Remove-AzHealthcareApisService -ResourceId $ResourceId
```

<span data-ttu-id="ad6bf-114">Удаляет существующую службу HealthcareApis с указанным ResourceId.</span><span class="sxs-lookup"><span data-stu-id="ad6bf-114">Deletes the existing HealthcareApis service with the provided ResourceId.</span></span>

### <span data-ttu-id="ad6bf-115">Пример 3</span><span class="sxs-lookup"><span data-stu-id="ad6bf-115">Example 3</span></span>
```powershell
PS C:\> Get-AzHealthcareApisService -ResourceGroupName MyResourceGroup -Name MyService | Remove-AzHealthcareApisService
```

<span data-ttu-id="ad6bf-116">Удаляет объект службы HealthcareApis, указанный в списке.</span><span class="sxs-lookup"><span data-stu-id="ad6bf-116">Deletes the provided HealthcareApis service object.</span></span>

## <span data-ttu-id="ad6bf-117">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="ad6bf-117">PARAMETERS</span></span>

### <span data-ttu-id="ad6bf-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ad6bf-118">-AsJob</span></span>
<span data-ttu-id="ad6bf-119">Запустите командлет как задание в фоновом режиме.</span><span class="sxs-lookup"><span data-stu-id="ad6bf-119">Run cmdlet as a job in the background.</span></span>

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

### <span data-ttu-id="ad6bf-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ad6bf-120">-DefaultProfile</span></span>
<span data-ttu-id="ad6bf-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="ad6bf-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ad6bf-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ad6bf-122">-InputObject</span></span>
<span data-ttu-id="ad6bf-123">Объект обслуживания HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="ad6bf-123">HealthcareApis service object</span></span>

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

### <span data-ttu-id="ad6bf-124">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="ad6bf-124">-Name</span></span>
<span data-ttu-id="ad6bf-125">Имя службы HealthcareApis.</span><span class="sxs-lookup"><span data-stu-id="ad6bf-125">HealthcareApis Service Name.</span></span>

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

### <span data-ttu-id="ad6bf-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ad6bf-126">-PassThru</span></span>
<span data-ttu-id="ad6bf-127">Если он указан, возвращает значение истина, если операция выполнена успешно</span><span class="sxs-lookup"><span data-stu-id="ad6bf-127">If provided, returns true if the operation was successful</span></span>

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

### <span data-ttu-id="ad6bf-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ad6bf-128">-ResourceGroupName</span></span>
<span data-ttu-id="ad6bf-129">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="ad6bf-129">Resource Group Name.</span></span>

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

### <span data-ttu-id="ad6bf-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ad6bf-130">-ResourceId</span></span>
<span data-ttu-id="ad6bf-131">HealthcareApis Service ResourceId.</span><span class="sxs-lookup"><span data-stu-id="ad6bf-131">HealthcareApis Service ResourceId.</span></span>

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

### <span data-ttu-id="ad6bf-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ad6bf-132">-Confirm</span></span>
<span data-ttu-id="ad6bf-133">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="ad6bf-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ad6bf-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ad6bf-134">-WhatIf</span></span>
<span data-ttu-id="ad6bf-135">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="ad6bf-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ad6bf-136">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="ad6bf-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ad6bf-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ad6bf-137">CommonParameters</span></span>
<span data-ttu-id="ad6bf-138">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="ad6bf-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ad6bf-139">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ad6bf-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ad6bf-140">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="ad6bf-140">INPUTS</span></span>

### <span data-ttu-id="ad6bf-141">System. String</span><span class="sxs-lookup"><span data-stu-id="ad6bf-141">System.String</span></span>

### <span data-ttu-id="ad6bf-142">Microsoft. Azure. Commands. HealthcareApisService. Models. PSHealthcareApisService</span><span class="sxs-lookup"><span data-stu-id="ad6bf-142">Microsoft.Azure.Commands.HealthcareApisService.Models.PSHealthcareApisService</span></span>

## <span data-ttu-id="ad6bf-143">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="ad6bf-143">OUTPUTS</span></span>

### <span data-ttu-id="ad6bf-144">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="ad6bf-144">System.Boolean</span></span>

## <span data-ttu-id="ad6bf-145">Пуск</span><span class="sxs-lookup"><span data-stu-id="ad6bf-145">NOTES</span></span>

## <span data-ttu-id="ad6bf-146">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ad6bf-146">RELATED LINKS</span></span>
