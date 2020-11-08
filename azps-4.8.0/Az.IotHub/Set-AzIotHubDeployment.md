---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/set-aziothubdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Set-AzIotHubDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Set-AzIotHubDeployment.md
ms.openlocfilehash: 1fac3ef0db0022bcb837392bf1c0b64e63c40401
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94079040"
---
# <span data-ttu-id="d955b-101">Set-AzIotHubDeployment</span><span class="sxs-lookup"><span data-stu-id="d955b-101">Set-AzIotHubDeployment</span></span>

## <span data-ttu-id="d955b-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="d955b-102">SYNOPSIS</span></span>
<span data-ttu-id="d955b-103">Обновите изменяемые поля в развертывании в Интернет – EDGE.</span><span class="sxs-lookup"><span data-stu-id="d955b-103">Update the mutable fields of IoT Edge deployment.</span></span>

## <span data-ttu-id="d955b-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="d955b-104">SYNTAX</span></span>

### <span data-ttu-id="d955b-105">Источник данных (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="d955b-105">ResourceSet (Default)</span></span>
```
Set-AzIotHubDeployment [-ResourceGroupName] <String> [-IotHubName] <String> -Name <String> [-Priority <Int32>]
 [-TargetCondition <String>] [-Metric <Hashtable>] [-Label <Hashtable>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d955b-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="d955b-106">InputObjectSet</span></span>
```
Set-AzIotHubDeployment [-InputObject] <PSIotHub> -Name <String> [-Priority <Int32>] [-TargetCondition <String>]
 [-Metric <Hashtable>] [-Label <Hashtable>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d955b-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="d955b-107">ResourceIdSet</span></span>
```
Set-AzIotHubDeployment [-ResourceId] <String> -Name <String> [-Priority <Int32>] [-TargetCondition <String>]
 [-Metric <Hashtable>] [-Label <Hashtable>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d955b-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d955b-108">DESCRIPTION</span></span>
<span data-ttu-id="d955b-109">Обновление указанных свойств развертывания в Интернет – EDGE.</span><span class="sxs-lookup"><span data-stu-id="d955b-109">Update specified properties of an IoT Edge deployment.</span></span>
<span data-ttu-id="d955b-110">Примечание. содержимое конфигурации является неизменяемым.</span><span class="sxs-lookup"><span data-stu-id="d955b-110">Note: Configuration content is immutable.</span></span> <span data-ttu-id="d955b-111">Свойства конфигурации, которые можно обновить: "метки", "метрики", "приоритет" и "targetCondition".</span><span class="sxs-lookup"><span data-stu-id="d955b-111">Configuration properties that can be updated are 'labels', 'metrics', 'priority' and 'targetCondition'.</span></span>
<span data-ttu-id="d955b-112"> https://docs.microsoft.com/azure/iot-edge/module-deployment-monitoringДля получения дополнительных сведений ознакомьтесь с дополнительными сведениями.</span><span class="sxs-lookup"><span data-stu-id="d955b-112">See https://docs.microsoft.com/azure/iot-edge/module-deployment-monitoring  for more information.</span></span>

## <span data-ttu-id="d955b-113">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="d955b-113">EXAMPLES</span></span>

### <span data-ttu-id="d955b-114">Пример 1</span><span class="sxs-lookup"><span data-stu-id="d955b-114">Example 1</span></span>
```powershell
PS C:\> Set-AzIotHubDeployment -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Name "deploy1" -Priority 7 -TargetCondition "tags.building=3 and tags.environment='dev'"
```

<span data-ttu-id="d955b-115">Измените приоритет развертывания Microsoft EDGE и обновите его целевое состояние.</span><span class="sxs-lookup"><span data-stu-id="d955b-115">Alter the priority of IoT Edge deployment and update its target condition.</span></span>

## <span data-ttu-id="d955b-116">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="d955b-116">PARAMETERS</span></span>

### <span data-ttu-id="d955b-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d955b-117">-DefaultProfile</span></span>
<span data-ttu-id="d955b-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="d955b-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d955b-119">-Force</span><span class="sxs-lookup"><span data-stu-id="d955b-119">-Force</span></span>
<span data-ttu-id="d955b-120">Позволяет заменять объект развертывания, даже если он был обновлен после того, как он был получен в прошлый раз.</span><span class="sxs-lookup"><span data-stu-id="d955b-120">Allows deployment object to be replaced even if it was updated since it was retrieved last time.</span></span>

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

### <span data-ttu-id="d955b-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d955b-121">-InputObject</span></span>
<span data-ttu-id="d955b-122">Объект IotHub</span><span class="sxs-lookup"><span data-stu-id="d955b-122">IotHub object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub
Parameter Sets: InputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d955b-123">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="d955b-123">-IotHubName</span></span>
<span data-ttu-id="d955b-124">Имя центра Интернета вещей</span><span class="sxs-lookup"><span data-stu-id="d955b-124">Name of the Iot Hub</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d955b-125">-Label</span><span class="sxs-lookup"><span data-stu-id="d955b-125">-Label</span></span>
<span data-ttu-id="d955b-126">Сопоставление меток, применяемых к целевому развертыванию.</span><span class="sxs-lookup"><span data-stu-id="d955b-126">Map of labels to be applied to target deployment.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d955b-127">-Метрическая система мер</span><span class="sxs-lookup"><span data-stu-id="d955b-127">-Metric</span></span>
<span data-ttu-id="d955b-128">Коллекция запросов с определением метрик развертывания для EDGE в IoT.</span><span class="sxs-lookup"><span data-stu-id="d955b-128">Queries collection for IoT Edge deployment metrics definition.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d955b-129">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="d955b-129">-Name</span></span>
<span data-ttu-id="d955b-130">Идентификатор развертывания.</span><span class="sxs-lookup"><span data-stu-id="d955b-130">Identifier for the deployment.</span></span>

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

### <span data-ttu-id="d955b-131">-Priority (приоритет)</span><span class="sxs-lookup"><span data-stu-id="d955b-131">-Priority</span></span>
<span data-ttu-id="d955b-132">Вес развертывания в случае с правилами конкурирующих конкурентов (самый высокий уровень WINS).</span><span class="sxs-lookup"><span data-stu-id="d955b-132">Weight of deployment in case of competing rules (highest wins).</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d955b-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d955b-133">-ResourceGroupName</span></span>
<span data-ttu-id="d955b-134">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="d955b-134">Name of the Resource Group</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d955b-135">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d955b-135">-ResourceId</span></span>
<span data-ttu-id="d955b-136">Идентификатор ресурса IotHub</span><span class="sxs-lookup"><span data-stu-id="d955b-136">IotHub Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d955b-137">-TargetCondition</span><span class="sxs-lookup"><span data-stu-id="d955b-137">-TargetCondition</span></span>
<span data-ttu-id="d955b-138">Целевое условие, к которому применяется развертывание Edge.</span><span class="sxs-lookup"><span data-stu-id="d955b-138">Target condition in which an Edge deployment applies to.</span></span>

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

### <span data-ttu-id="d955b-139">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d955b-139">-Confirm</span></span>
<span data-ttu-id="d955b-140">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="d955b-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d955b-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d955b-141">-WhatIf</span></span>
<span data-ttu-id="d955b-142">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="d955b-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d955b-143">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="d955b-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d955b-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d955b-144">CommonParameters</span></span>
<span data-ttu-id="d955b-145">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="d955b-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d955b-146">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d955b-146">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d955b-147">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="d955b-147">INPUTS</span></span>

### <span data-ttu-id="d955b-148">Microsoft. Azure. Commands. Management. IotHub. Models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="d955b-148">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="d955b-149">System. String</span><span class="sxs-lookup"><span data-stu-id="d955b-149">System.String</span></span>

## <span data-ttu-id="d955b-150">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="d955b-150">OUTPUTS</span></span>

### <span data-ttu-id="d955b-151">Microsoft.Azure.Commands.Management.IotHub.Models.PSDeployment</span><span class="sxs-lookup"><span data-stu-id="d955b-151">Microsoft.Azure.Commands.Management.IotHub.Models.PSDeployment</span></span>

## <span data-ttu-id="d955b-152">Пуск</span><span class="sxs-lookup"><span data-stu-id="d955b-152">NOTES</span></span>

## <span data-ttu-id="d955b-153">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d955b-153">RELATED LINKS</span></span>
