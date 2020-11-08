---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/remove-aziothubdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHubDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHubDeployment.md
ms.openlocfilehash: f5463015b93c209c6cf8952c566e9656da2fba18
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94245329"
---
# <span data-ttu-id="913ed-101">Remove-AzIotHubDeployment</span><span class="sxs-lookup"><span data-stu-id="913ed-101">Remove-AzIotHubDeployment</span></span>

## <span data-ttu-id="913ed-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="913ed-102">SYNOPSIS</span></span>
<span data-ttu-id="913ed-103">Удалите развертывание с краем IoT.</span><span class="sxs-lookup"><span data-stu-id="913ed-103">Delete an IoT Edge deployment.</span></span>

## <span data-ttu-id="913ed-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="913ed-104">SYNTAX</span></span>

### <span data-ttu-id="913ed-105">Источник данных (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="913ed-105">ResourceSet (Default)</span></span>
```
Remove-AzIotHubDeployment [-ResourceGroupName] <String> [-IotHubName] <String> [-Name <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="913ed-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="913ed-106">InputObjectSet</span></span>
```
Remove-AzIotHubDeployment [-InputObject] <PSIotHub> [-Name <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="913ed-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="913ed-107">ResourceIdSet</span></span>
```
Remove-AzIotHubDeployment [-ResourceId] <String> [-Name <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="913ed-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="913ed-108">DESCRIPTION</span></span>
<span data-ttu-id="913ed-109"> https://docs.microsoft.com/azure/iot-edge/module-deployment-monitoringДля получения дополнительных сведений ознакомьтесь с дополнительными сведениями.</span><span class="sxs-lookup"><span data-stu-id="913ed-109">See https://docs.microsoft.com/azure/iot-edge/module-deployment-monitoring for more information.</span></span>

## <span data-ttu-id="913ed-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="913ed-110">EXAMPLES</span></span>

### <span data-ttu-id="913ed-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="913ed-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzIotHubDeployment -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Name "deploy1"
```

<span data-ttu-id="913ed-112">Удалите развертывание с краем IoT.</span><span class="sxs-lookup"><span data-stu-id="913ed-112">Delete an IoT Edge deployment.</span></span>

## <span data-ttu-id="913ed-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="913ed-113">PARAMETERS</span></span>

### <span data-ttu-id="913ed-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="913ed-114">-DefaultProfile</span></span>
<span data-ttu-id="913ed-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="913ed-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="913ed-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="913ed-116">-InputObject</span></span>
<span data-ttu-id="913ed-117">Объект IotHub</span><span class="sxs-lookup"><span data-stu-id="913ed-117">IotHub object</span></span>

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

### <span data-ttu-id="913ed-118">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="913ed-118">-IotHubName</span></span>
<span data-ttu-id="913ed-119">Имя центра Интернета вещей</span><span class="sxs-lookup"><span data-stu-id="913ed-119">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="913ed-120">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="913ed-120">-Name</span></span>
<span data-ttu-id="913ed-121">Идентификатор развертывания.</span><span class="sxs-lookup"><span data-stu-id="913ed-121">Identifier for the deployment.</span></span>

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

### <span data-ttu-id="913ed-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="913ed-122">-PassThru</span></span>
<span data-ttu-id="913ed-123">Позволяет возвращать логический объект.</span><span class="sxs-lookup"><span data-stu-id="913ed-123">Allows to return the boolean object.</span></span>
<span data-ttu-id="913ed-124">По умолчанию этот командлет не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="913ed-124">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="913ed-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="913ed-125">-ResourceGroupName</span></span>
<span data-ttu-id="913ed-126">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="913ed-126">Name of the Resource Group</span></span>

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

### <span data-ttu-id="913ed-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="913ed-127">-ResourceId</span></span>
<span data-ttu-id="913ed-128">Идентификатор ресурса IotHub</span><span class="sxs-lookup"><span data-stu-id="913ed-128">IotHub Resource Id</span></span>

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

### <span data-ttu-id="913ed-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="913ed-129">-Confirm</span></span>
<span data-ttu-id="913ed-130">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="913ed-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="913ed-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="913ed-131">-WhatIf</span></span>
<span data-ttu-id="913ed-132">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="913ed-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="913ed-133">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="913ed-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="913ed-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="913ed-134">CommonParameters</span></span>
<span data-ttu-id="913ed-135">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="913ed-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="913ed-136">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="913ed-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="913ed-137">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="913ed-137">INPUTS</span></span>

### <span data-ttu-id="913ed-138">Microsoft. Azure. Commands. Management. IotHub. Models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="913ed-138">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="913ed-139">System. String</span><span class="sxs-lookup"><span data-stu-id="913ed-139">System.String</span></span>

## <span data-ttu-id="913ed-140">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="913ed-140">OUTPUTS</span></span>

### <span data-ttu-id="913ed-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="913ed-141">System.Boolean</span></span>

## <span data-ttu-id="913ed-142">Пуск</span><span class="sxs-lookup"><span data-stu-id="913ed-142">NOTES</span></span>

## <span data-ttu-id="913ed-143">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="913ed-143">RELATED LINKS</span></span>
