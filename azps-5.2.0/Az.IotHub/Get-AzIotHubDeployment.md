---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothubdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubDeployment.md
ms.openlocfilehash: 1440b77d753a27b1c2a7176be5b44ef69fca2e50
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98391119"
---
# <span data-ttu-id="46e55-101">Get-AzIotHubDeployment</span><span class="sxs-lookup"><span data-stu-id="46e55-101">Get-AzIotHubDeployment</span></span>

## <span data-ttu-id="46e55-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="46e55-102">SYNOPSIS</span></span>
<span data-ttu-id="46e55-103">Здесь перечислены все или только определенные развертывания IoT Edge.</span><span class="sxs-lookup"><span data-stu-id="46e55-103">Lists all or a particular IoT Edge deployment.</span></span>

## <span data-ttu-id="46e55-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="46e55-104">SYNTAX</span></span>

### <span data-ttu-id="46e55-105">Набор ресурсов (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="46e55-105">ResourceSet (Default)</span></span>
```
Get-AzIotHubDeployment [-ResourceGroupName] <String> [-IotHubName] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="46e55-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="46e55-106">InputObjectSet</span></span>
```
Get-AzIotHubDeployment [-InputObject] <PSIotHub> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="46e55-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="46e55-107">ResourceIdSet</span></span>
```
Get-AzIotHubDeployment [-ResourceId] <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="46e55-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="46e55-108">DESCRIPTION</span></span>
<span data-ttu-id="46e55-109">Подробные сведения о развертывании IoT Edge или развертывании List IoT Edge в центре IoT.</span><span class="sxs-lookup"><span data-stu-id="46e55-109">Get the details of an IoT Edge deployment or List IoT Edge deployments in an IoT Hub.</span></span>
<span data-ttu-id="46e55-110">Дополнительные https://docs.microsoft.com/azure/iot-edge/module-deployment-monitoring сведения см. в этой информации.</span><span class="sxs-lookup"><span data-stu-id="46e55-110">See https://docs.microsoft.com/azure/iot-edge/module-deployment-monitoring for more information.</span></span>

## <span data-ttu-id="46e55-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="46e55-111">EXAMPLES</span></span>

### <span data-ttu-id="46e55-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="46e55-112">Example 1</span></span>
```powershell
PS C:\> Get-AzIotHubDeployment -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Name "deploy1"
```

<span data-ttu-id="46e55-113">Получите подробные сведения о развертывании IoT Edge.</span><span class="sxs-lookup"><span data-stu-id="46e55-113">Get the details of an IoT Edge deployment.</span></span>

### <span data-ttu-id="46e55-114">Пример 2</span><span class="sxs-lookup"><span data-stu-id="46e55-114">Example 2</span></span>
```powershell
PS C:\> Get-AzIotHubDeployment -ResourceGroupName "myresourcegroup" -IotHubName "myiothub"
```

<span data-ttu-id="46e55-115">Перечислите все развертывания IoT Edge в центре IoT.</span><span class="sxs-lookup"><span data-stu-id="46e55-115">List all IoT Edge deployments in an IoT Hub.</span></span>

## <span data-ttu-id="46e55-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="46e55-116">PARAMETERS</span></span>

### <span data-ttu-id="46e55-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="46e55-117">-DefaultProfile</span></span>
<span data-ttu-id="46e55-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="46e55-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="46e55-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="46e55-119">-InputObject</span></span>
<span data-ttu-id="46e55-120">Объект IotHub</span><span class="sxs-lookup"><span data-stu-id="46e55-120">IotHub object</span></span>

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

### <span data-ttu-id="46e55-121">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="46e55-121">-IotHubName</span></span>
<span data-ttu-id="46e55-122">Имя концентратора Iot</span><span class="sxs-lookup"><span data-stu-id="46e55-122">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="46e55-123">-Name</span><span class="sxs-lookup"><span data-stu-id="46e55-123">-Name</span></span>
<span data-ttu-id="46e55-124">Идентификатор развертывания.</span><span class="sxs-lookup"><span data-stu-id="46e55-124">Identifier for the deployment.</span></span>

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

### <span data-ttu-id="46e55-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="46e55-125">-ResourceGroupName</span></span>
<span data-ttu-id="46e55-126">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="46e55-126">Name of the Resource Group</span></span>

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

### <span data-ttu-id="46e55-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="46e55-127">-ResourceId</span></span>
<span data-ttu-id="46e55-128">ИД ресурса IotHub</span><span class="sxs-lookup"><span data-stu-id="46e55-128">IotHub Resource Id</span></span>

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

### <span data-ttu-id="46e55-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="46e55-129">CommonParameters</span></span>
<span data-ttu-id="46e55-130">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="46e55-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="46e55-131">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="46e55-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="46e55-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="46e55-132">INPUTS</span></span>

### <span data-ttu-id="46e55-133">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="46e55-133">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="46e55-134">System.String</span><span class="sxs-lookup"><span data-stu-id="46e55-134">System.String</span></span>

## <span data-ttu-id="46e55-135">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="46e55-135">OUTPUTS</span></span>

### <span data-ttu-id="46e55-136">Microsoft.Azure.Commands.Management.IotHub.Models.PSDвслух</span><span class="sxs-lookup"><span data-stu-id="46e55-136">Microsoft.Azure.Commands.Management.IotHub.Models.PSDeployment</span></span>

### <span data-ttu-id="46e55-137">Microsoft.Azure.Commands.Management.IotHub.Models.PSDeployments[]</span><span class="sxs-lookup"><span data-stu-id="46e55-137">Microsoft.Azure.Commands.Management.IotHub.Models.PSDeployments[]</span></span>

## <span data-ttu-id="46e55-138">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="46e55-138">NOTES</span></span>

## <span data-ttu-id="46e55-139">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="46e55-139">RELATED LINKS</span></span>
