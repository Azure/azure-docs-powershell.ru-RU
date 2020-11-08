---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothubdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubDeployment.md
ms.openlocfilehash: 1440b77d753a27b1c2a7176be5b44ef69fca2e50
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94247756"
---
# <span data-ttu-id="aad92-101">Get-AzIotHubDeployment</span><span class="sxs-lookup"><span data-stu-id="aad92-101">Get-AzIotHubDeployment</span></span>

## <span data-ttu-id="aad92-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="aad92-102">SYNOPSIS</span></span>
<span data-ttu-id="aad92-103">Список всех или определенных развертываний в Интернет-EDGE.</span><span class="sxs-lookup"><span data-stu-id="aad92-103">Lists all or a particular IoT Edge deployment.</span></span>

## <span data-ttu-id="aad92-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="aad92-104">SYNTAX</span></span>

### <span data-ttu-id="aad92-105">Источник данных (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="aad92-105">ResourceSet (Default)</span></span>
```
Get-AzIotHubDeployment [-ResourceGroupName] <String> [-IotHubName] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="aad92-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="aad92-106">InputObjectSet</span></span>
```
Get-AzIotHubDeployment [-InputObject] <PSIotHub> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="aad92-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="aad92-107">ResourceIdSet</span></span>
```
Get-AzIotHubDeployment [-ResourceId] <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="aad92-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="aad92-108">DESCRIPTION</span></span>
<span data-ttu-id="aad92-109">Ознакомьтесь с подробностями развертывания и списка развернутых серверов Интернета вещей в центре Интернета вещей.</span><span class="sxs-lookup"><span data-stu-id="aad92-109">Get the details of an IoT Edge deployment or List IoT Edge deployments in an IoT Hub.</span></span>
<span data-ttu-id="aad92-110"> https://docs.microsoft.com/azure/iot-edge/module-deployment-monitoringДля получения дополнительных сведений ознакомьтесь с дополнительными сведениями.</span><span class="sxs-lookup"><span data-stu-id="aad92-110">See https://docs.microsoft.com/azure/iot-edge/module-deployment-monitoring for more information.</span></span>

## <span data-ttu-id="aad92-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="aad92-111">EXAMPLES</span></span>

### <span data-ttu-id="aad92-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="aad92-112">Example 1</span></span>
```powershell
PS C:\> Get-AzIotHubDeployment -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Name "deploy1"
```

<span data-ttu-id="aad92-113">Получение сведений о развертывании в Интернет – EDGE.</span><span class="sxs-lookup"><span data-stu-id="aad92-113">Get the details of an IoT Edge deployment.</span></span>

### <span data-ttu-id="aad92-114">Пример 2</span><span class="sxs-lookup"><span data-stu-id="aad92-114">Example 2</span></span>
```powershell
PS C:\> Get-AzIotHubDeployment -ResourceGroupName "myresourcegroup" -IotHubName "myiothub"
```

<span data-ttu-id="aad92-115">Перечислите все развертывания по краям в IoT в центре Интернета вещей.</span><span class="sxs-lookup"><span data-stu-id="aad92-115">List all IoT Edge deployments in an IoT Hub.</span></span>

## <span data-ttu-id="aad92-116">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="aad92-116">PARAMETERS</span></span>

### <span data-ttu-id="aad92-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aad92-117">-DefaultProfile</span></span>
<span data-ttu-id="aad92-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="aad92-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="aad92-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="aad92-119">-InputObject</span></span>
<span data-ttu-id="aad92-120">Объект IotHub</span><span class="sxs-lookup"><span data-stu-id="aad92-120">IotHub object</span></span>

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

### <span data-ttu-id="aad92-121">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="aad92-121">-IotHubName</span></span>
<span data-ttu-id="aad92-122">Имя центра Интернета вещей</span><span class="sxs-lookup"><span data-stu-id="aad92-122">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="aad92-123">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="aad92-123">-Name</span></span>
<span data-ttu-id="aad92-124">Идентификатор развертывания.</span><span class="sxs-lookup"><span data-stu-id="aad92-124">Identifier for the deployment.</span></span>

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

### <span data-ttu-id="aad92-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="aad92-125">-ResourceGroupName</span></span>
<span data-ttu-id="aad92-126">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="aad92-126">Name of the Resource Group</span></span>

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

### <span data-ttu-id="aad92-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="aad92-127">-ResourceId</span></span>
<span data-ttu-id="aad92-128">Идентификатор ресурса IotHub</span><span class="sxs-lookup"><span data-stu-id="aad92-128">IotHub Resource Id</span></span>

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

### <span data-ttu-id="aad92-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aad92-129">CommonParameters</span></span>
<span data-ttu-id="aad92-130">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="aad92-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aad92-131">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="aad92-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aad92-132">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="aad92-132">INPUTS</span></span>

### <span data-ttu-id="aad92-133">Microsoft. Azure. Commands. Management. IotHub. Models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="aad92-133">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="aad92-134">System. String</span><span class="sxs-lookup"><span data-stu-id="aad92-134">System.String</span></span>

## <span data-ttu-id="aad92-135">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="aad92-135">OUTPUTS</span></span>

### <span data-ttu-id="aad92-136">Microsoft.Azure.Commands.Management.IotHub.Models.PSDeployment</span><span class="sxs-lookup"><span data-stu-id="aad92-136">Microsoft.Azure.Commands.Management.IotHub.Models.PSDeployment</span></span>

### <span data-ttu-id="aad92-137">Microsoft.Azure.Commands.Management.IotHub.Models.PSDeployments []</span><span class="sxs-lookup"><span data-stu-id="aad92-137">Microsoft.Azure.Commands.Management.IotHub.Models.PSDeployments[]</span></span>

## <span data-ttu-id="aad92-138">Пуск</span><span class="sxs-lookup"><span data-stu-id="aad92-138">NOTES</span></span>

## <span data-ttu-id="aad92-139">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="aad92-139">RELATED LINKS</span></span>
