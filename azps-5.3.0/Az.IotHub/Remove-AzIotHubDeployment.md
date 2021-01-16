---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/remove-aziothubdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHubDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHubDeployment.md
ms.openlocfilehash: f5463015b93c209c6cf8952c566e9656da2fba18
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98426055"
---
# <span data-ttu-id="d81e6-101">Remove-AzIotHubDeployment</span><span class="sxs-lookup"><span data-stu-id="d81e6-101">Remove-AzIotHubDeployment</span></span>

## <span data-ttu-id="d81e6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d81e6-102">SYNOPSIS</span></span>
<span data-ttu-id="d81e6-103">Удалите развертывание IoT Edge.</span><span class="sxs-lookup"><span data-stu-id="d81e6-103">Delete an IoT Edge deployment.</span></span>

## <span data-ttu-id="d81e6-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="d81e6-104">SYNTAX</span></span>

### <span data-ttu-id="d81e6-105">Набор ресурсов (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="d81e6-105">ResourceSet (Default)</span></span>
```
Remove-AzIotHubDeployment [-ResourceGroupName] <String> [-IotHubName] <String> [-Name <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d81e6-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="d81e6-106">InputObjectSet</span></span>
```
Remove-AzIotHubDeployment [-InputObject] <PSIotHub> [-Name <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d81e6-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="d81e6-107">ResourceIdSet</span></span>
```
Remove-AzIotHubDeployment [-ResourceId] <String> [-Name <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d81e6-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d81e6-108">DESCRIPTION</span></span>
<span data-ttu-id="d81e6-109">Дополнительные https://docs.microsoft.com/azure/iot-edge/module-deployment-monitoring сведения см. в этой области.</span><span class="sxs-lookup"><span data-stu-id="d81e6-109">See https://docs.microsoft.com/azure/iot-edge/module-deployment-monitoring for more information.</span></span>

## <span data-ttu-id="d81e6-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="d81e6-110">EXAMPLES</span></span>

### <span data-ttu-id="d81e6-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="d81e6-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzIotHubDeployment -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Name "deploy1"
```

<span data-ttu-id="d81e6-112">Удалите развертывание IoT Edge.</span><span class="sxs-lookup"><span data-stu-id="d81e6-112">Delete an IoT Edge deployment.</span></span>

## <span data-ttu-id="d81e6-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d81e6-113">PARAMETERS</span></span>

### <span data-ttu-id="d81e6-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d81e6-114">-DefaultProfile</span></span>
<span data-ttu-id="d81e6-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="d81e6-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d81e6-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d81e6-116">-InputObject</span></span>
<span data-ttu-id="d81e6-117">Объект IotHub</span><span class="sxs-lookup"><span data-stu-id="d81e6-117">IotHub object</span></span>

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

### <span data-ttu-id="d81e6-118">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="d81e6-118">-IotHubName</span></span>
<span data-ttu-id="d81e6-119">Имя концентратора Iot</span><span class="sxs-lookup"><span data-stu-id="d81e6-119">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="d81e6-120">-Name</span><span class="sxs-lookup"><span data-stu-id="d81e6-120">-Name</span></span>
<span data-ttu-id="d81e6-121">Идентификатор развертывания.</span><span class="sxs-lookup"><span data-stu-id="d81e6-121">Identifier for the deployment.</span></span>

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

### <span data-ttu-id="d81e6-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d81e6-122">-PassThru</span></span>
<span data-ttu-id="d81e6-123">Разрешает возвращать boolean object.</span><span class="sxs-lookup"><span data-stu-id="d81e6-123">Allows to return the boolean object.</span></span>
<span data-ttu-id="d81e6-124">По умолчанию этот cmdlet не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="d81e6-124">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="d81e6-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d81e6-125">-ResourceGroupName</span></span>
<span data-ttu-id="d81e6-126">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="d81e6-126">Name of the Resource Group</span></span>

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

### <span data-ttu-id="d81e6-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d81e6-127">-ResourceId</span></span>
<span data-ttu-id="d81e6-128">ИД ресурса IotHub</span><span class="sxs-lookup"><span data-stu-id="d81e6-128">IotHub Resource Id</span></span>

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

### <span data-ttu-id="d81e6-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d81e6-129">-Confirm</span></span>
<span data-ttu-id="d81e6-130">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d81e6-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d81e6-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d81e6-131">-WhatIf</span></span>
<span data-ttu-id="d81e6-132">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d81e6-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d81e6-133">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="d81e6-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d81e6-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d81e6-134">CommonParameters</span></span>
<span data-ttu-id="d81e6-135">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d81e6-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d81e6-136">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d81e6-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d81e6-137">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d81e6-137">INPUTS</span></span>

### <span data-ttu-id="d81e6-138">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="d81e6-138">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="d81e6-139">System.String</span><span class="sxs-lookup"><span data-stu-id="d81e6-139">System.String</span></span>

## <span data-ttu-id="d81e6-140">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="d81e6-140">OUTPUTS</span></span>

### <span data-ttu-id="d81e6-141">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="d81e6-141">System.Boolean</span></span>

## <span data-ttu-id="d81e6-142">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="d81e6-142">NOTES</span></span>

## <span data-ttu-id="d81e6-143">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d81e6-143">RELATED LINKS</span></span>
