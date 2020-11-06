---
external help file: Microsoft.Azure.Commands.ContainerInstance.dll-Help.xml
Module Name: AzureRM.ContainerInstance
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerInstance/Commands.ContainerInstance/help/Get-AzureRmContainerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerInstance/Commands.ContainerInstance/help/Get-AzureRmContainerGroup.md
ms.openlocfilehash: f97f7ca82ae17c61994a84fbc4b1405b41fdb566
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93570075"
---
# <span data-ttu-id="a80b2-101">Get-AzureRmContainerGroup</span><span class="sxs-lookup"><span data-stu-id="a80b2-101">Get-AzureRmContainerGroup</span></span>

## <span data-ttu-id="a80b2-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="a80b2-102">SYNOPSIS</span></span>
<span data-ttu-id="a80b2-103">Возвращает группы контейнеров.</span><span class="sxs-lookup"><span data-stu-id="a80b2-103">Gets container groups.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a80b2-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="a80b2-104">SYNTAX</span></span>

### <span data-ttu-id="a80b2-105">ListContainerGroupParamSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="a80b2-105">ListContainerGroupParamSet (Default)</span></span>
```
Get-AzureRmContainerGroup [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="a80b2-106">GetContainerGroupInResourceGroupParamSet</span><span class="sxs-lookup"><span data-stu-id="a80b2-106">GetContainerGroupInResourceGroupParamSet</span></span>
```
Get-AzureRmContainerGroup [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a80b2-107">GetContainerGroupByResourceIdParamSet</span><span class="sxs-lookup"><span data-stu-id="a80b2-107">GetContainerGroupByResourceIdParamSet</span></span>
```
Get-AzureRmContainerGroup -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a80b2-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a80b2-108">DESCRIPTION</span></span>
<span data-ttu-id="a80b2-109">Командлет **Get-AzureRmContainerGroup** получает указанную группу контейнеров или все группы контейнеров в группе ресурсов или подписке.</span><span class="sxs-lookup"><span data-stu-id="a80b2-109">The **Get-AzureRmContainerGroup** cmdlet gets a specified container group or all the container groups in a resource group or the subscription.</span></span>

## <span data-ttu-id="a80b2-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="a80b2-110">EXAMPLES</span></span>

### <span data-ttu-id="a80b2-111">Пример 1: получает указанную группу контейнеров.</span><span class="sxs-lookup"><span data-stu-id="a80b2-111">Example 1: Gets a specified container group</span></span>
```
PS C:\> Get-AzureRmContainerGroup -ResourceGroupName demo -Name mycontainer

ResourceGroupName        : demo
Id                       : /subscriptions/ae43b1e3-c35d-4c8c-bc0d-f148b4c52b78/resourceGroups/demo/providers/Microsoft.ContainerInstance/containerGroups/mycontainer
Name                     : mycontainer
Type                     : Microsoft.ContainerInstance/containerGroups
Location                 : westus
Tags                     :
ProvisioningState        : Succeeded
Containers               : {mycontainer}
ImageRegistryCredentials :
RestartPolicy            :
IpAddress                : 13.88.10.240
Ports                    : {8000}
OsType                   : Linux
Volumes                  :
```

<span data-ttu-id="a80b2-112">Команда получает указанную группу контейнеров.</span><span class="sxs-lookup"><span data-stu-id="a80b2-112">The command gets the specified container group.</span></span>

### <span data-ttu-id="a80b2-113">Пример 2: получение групп контейнеров в группе ресурсов</span><span class="sxs-lookup"><span data-stu-id="a80b2-113">Example 2: Gets container groups in a resource group</span></span>
```
PS C:\> Get-AzureRmContainerGroup -ResourceGroupName demo

ResourceGroupName Name                     Location   OsType  Image                         IP                   Resources        ProvisioningState
----------------- ----                     --------   ------  -----                         --                   ---------        -----------------
demo              container1               west us    Linux   alpine:latest                 40.83.144.50:8002    1 cores/1 gb             Succeeded
demo              container2               west us    Linux   alpine:latest                 104.42.228.253:8001  1 cores/1 gb             Succeeded
```

<span data-ttu-id="a80b2-114">Команда получает группы контейнеров в группе ресурсов `demo` .</span><span class="sxs-lookup"><span data-stu-id="a80b2-114">The command gets the container groups in the resource group `demo`.</span></span>

### <span data-ttu-id="a80b2-115">Пример 3: получение групп контейнеров в текущей подписке</span><span class="sxs-lookup"><span data-stu-id="a80b2-115">Example 3: Gets container groups in the current subscription</span></span>
```
PS C:\> Get-AzureRmContainerGroup

ResourceGroupName Name                     Location   OsType  Image                         IP                   Resources        ProvisioningState
----------------- ----                     --------   ------  -----                         --                   ---------        -----------------
demo1             container1               west us    Linux   alpine:latest                 40.83.144.50:8002    1 cores/1 gb             Succeeded
demo2             container2               west us    Linux   alpine:latest                 104.42.228.253:8001  1 cores/1 gb             Succeeded
```

<span data-ttu-id="a80b2-116">Команда получает группы контейнеров в текущей подписке.</span><span class="sxs-lookup"><span data-stu-id="a80b2-116">The command gets the container groups in the current subscription.</span></span>

### <span data-ttu-id="a80b2-117">Пример 4: получение групп контейнеров с использованием идентификатора ресурса.</span><span class="sxs-lookup"><span data-stu-id="a80b2-117">Example 4: Gets container groups using resource Id.</span></span>
```
PS C:\> Find-AzureRmResource -ResourceGroupEquals demo -ResourceNameEquals mycontainer | Get-AzureRmContainerGroup

ResourceGroupName        : demo
Id                       : /subscriptions/ae43b1e3-c35d-4c8c-bc0d-f148b4c52b78/resourceGroups/demo/providers/Microsoft.ContainerInstance/containerGroups/mycontainer
Name                     : mycontainer
Type                     : Microsoft.ContainerInstance/containerGroups
Location                 : westus
Tags                     :
ProvisioningState        : Succeeded
Containers               : {mycontainer}
ImageRegistryCredentials :
RestartPolicy            :
IpAddress                : 13.88.10.240
Ports                    : {8000}
OsType                   : Linux
Volumes                  :
```

<span data-ttu-id="a80b2-118">Команда получает группу контейнеров с идентификатором ресурса.</span><span class="sxs-lookup"><span data-stu-id="a80b2-118">The command gets the container group with the resource Id.</span></span>

## <span data-ttu-id="a80b2-119">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="a80b2-119">PARAMETERS</span></span>

### <span data-ttu-id="a80b2-120">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="a80b2-120">-Name</span></span>
<span data-ttu-id="a80b2-121">Имя группы контейнера.</span><span class="sxs-lookup"><span data-stu-id="a80b2-121">The container group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: GetContainerGroupInResourceGroupParamSet
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a80b2-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a80b2-122">-ResourceGroupName</span></span>
<span data-ttu-id="a80b2-123">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="a80b2-123">The resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: ListContainerGroupParamSet
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: GetContainerGroupInResourceGroupParamSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a80b2-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a80b2-124">-ResourceId</span></span>
<span data-ttu-id="a80b2-125">Идентификатор ресурса.</span><span class="sxs-lookup"><span data-stu-id="a80b2-125">The resource id.</span></span>

```yaml
Type: System.String
Parameter Sets: GetContainerGroupByResourceIdParamSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a80b2-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a80b2-126">-DefaultProfile</span></span>
<span data-ttu-id="a80b2-127">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="a80b2-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a80b2-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a80b2-128">CommonParameters</span></span>
<span data-ttu-id="a80b2-129">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="a80b2-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a80b2-130">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a80b2-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a80b2-131">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="a80b2-131">INPUTS</span></span>

### <span data-ttu-id="a80b2-132">System. String</span><span class="sxs-lookup"><span data-stu-id="a80b2-132">System.String</span></span>

## <span data-ttu-id="a80b2-133">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="a80b2-133">OUTPUTS</span></span>

### <span data-ttu-id="a80b2-134">Microsoft. Azure. Commands. ContainerInstance. Models. PSContainerGroup</span><span class="sxs-lookup"><span data-stu-id="a80b2-134">Microsoft.Azure.Commands.ContainerInstance.Models.PSContainerGroup</span></span>

## <span data-ttu-id="a80b2-135">Пуск</span><span class="sxs-lookup"><span data-stu-id="a80b2-135">NOTES</span></span>

## <span data-ttu-id="a80b2-136">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a80b2-136">RELATED LINKS</span></span>

