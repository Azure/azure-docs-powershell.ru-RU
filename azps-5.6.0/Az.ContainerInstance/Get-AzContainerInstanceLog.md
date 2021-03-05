---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerInstance.dll-Help.xml
Module Name: Az.ContainerInstance
online version: https://docs.microsoft.com/powershell/module/az.containerinstance/get-azcontainerinstancelog
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerInstance/ContainerInstance/help/Get-AzContainerInstanceLog.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerInstance/ContainerInstance/help/Get-AzContainerInstanceLog.md
ms.openlocfilehash: 2ab0102534a8773ca1ca206bde2075e2bd7930f4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102012259"
---
# <span data-ttu-id="9d299-101">Get-AzContainerInstanceLog</span><span class="sxs-lookup"><span data-stu-id="9d299-101">Get-AzContainerInstanceLog</span></span>

## <span data-ttu-id="9d299-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9d299-102">SYNOPSIS</span></span>
<span data-ttu-id="9d299-103">Получить журналы экземпляра контейнера в группе контейнеров.</span><span class="sxs-lookup"><span data-stu-id="9d299-103">Get the logs of a container instance in a container group.</span></span>

## <span data-ttu-id="9d299-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="9d299-104">SYNTAX</span></span>

### <span data-ttu-id="9d299-105">GetContainerInstanceLogByNamesParamSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="9d299-105">GetContainerInstanceLogByNamesParamSet (Default)</span></span>
```
Get-AzContainerInstanceLog [-ResourceGroupName] <String> -ContainerGroupName <String> [-Name <String>]
 [-Tail <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9d299-106">GetContainerInstanceLogByPSContainerGroupParamSet</span><span class="sxs-lookup"><span data-stu-id="9d299-106">GetContainerInstanceLogByPSContainerGroupParamSet</span></span>
```
Get-AzContainerInstanceLog -InputContainerGroup <PSContainerGroup> [-Name <String>] [-Tail <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9d299-107">GetContainerInstanceLogByResourceIdParamSet</span><span class="sxs-lookup"><span data-stu-id="9d299-107">GetContainerInstanceLogByResourceIdParamSet</span></span>
```
Get-AzContainerInstanceLog -ResourceId <String> [-Name <String>] [-Tail <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9d299-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="9d299-108">DESCRIPTION</span></span>
<span data-ttu-id="9d299-109">С **его учетом** можно получить журналы контейнера в группе контейнеров.</span><span class="sxs-lookup"><span data-stu-id="9d299-109">The **Get-AzContainerInstanceLog** cmdlet gets the logs of a container in a container group.</span></span>

## <span data-ttu-id="9d299-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="9d299-110">EXAMPLES</span></span>

### <span data-ttu-id="9d299-111">Пример 1. Получить журнал хвостов экземпляра контейнера</span><span class="sxs-lookup"><span data-stu-id="9d299-111">Example 1: Get the tail log of a container instance</span></span>
```
PS C:\> Get-AzContainerInstanceLog -ResourceGroupName demo -ContainerGroupName mycontainer -Name container1

Log line 1.
Log line 2.
Log line 3.
Log line 4.
```

<span data-ttu-id="9d299-112">Получить журнал в `container1` группе `mycontainer` контейнеров.</span><span class="sxs-lookup"><span data-stu-id="9d299-112">Get the log from `container1` in container group `mycontainer`.</span></span> <span data-ttu-id="9d299-113">По умолчанию в журнале возвращается до 4 МБ.</span><span class="sxs-lookup"><span data-stu-id="9d299-113">By default, it will return up to 4MB log content.</span></span>

### <span data-ttu-id="9d299-114">Пример 2. Получить журнал хвостов экземпляра контейнера, имя которого такое же, как у группы контейнеров</span><span class="sxs-lookup"><span data-stu-id="9d299-114">Example 2: Get the tail log of a container instance that has the same name as the container group</span></span>
```
PS C:\> Get-AzContainerInstanceLog -ResourceGroupName demo -ContainerGroupName mycontainer

Log line 1.
Log line 2.
Log line 3.
Log line 4.
```

<span data-ttu-id="9d299-115">Получить журнал в `mycontainer` группе `mycontainer` контейнеров.</span><span class="sxs-lookup"><span data-stu-id="9d299-115">Get the log from `mycontainer` in container group `mycontainer`.</span></span> <span data-ttu-id="9d299-116">По умолчанию в журнале возвращается до 4 МБ.</span><span class="sxs-lookup"><span data-stu-id="9d299-116">By default, it will return up to 4MB log content.</span></span>

### <span data-ttu-id="9d299-117">Пример 3. Получить хвост 2 строки журнала экземпляра контейнера</span><span class="sxs-lookup"><span data-stu-id="9d299-117">Example 3: Get the tail 2 lines of log of a container instance</span></span>
```
PS C:\> Get-AzContainerInstanceLog -ResourceGroupName demo -ContainerGroupName mycontainer -Name container1 -Tail 2

Log line 3.
Log line 4.
```

<span data-ttu-id="9d299-118">Получите хвосты 2 строки журнала в `container1` группе `mycontainer` контейнеров.</span><span class="sxs-lookup"><span data-stu-id="9d299-118">Get the tail 2 lines of log from `container1` in container group `mycontainer`.</span></span>

### <span data-ttu-id="9d299-119">Пример 4. Получить журнал хвостов экземпляра контейнера в трубе в группе контейнеров</span><span class="sxs-lookup"><span data-stu-id="9d299-119">Example 4: Get the tail log of a container instance in a piped in container group</span></span>
```
PS C:\> Get-AzContainerGroup -ResourceGroupName demo -Name mycontainer | Get-AzContainerInstanceLog

Log line 1.
Log line 2.
Log line 3.
Log line 4.
```

<span data-ttu-id="9d299-120">Получить журнал в канале `mycontainer` в группе `mycontainer` контейнеров.</span><span class="sxs-lookup"><span data-stu-id="9d299-120">Get the log from `mycontainer` in piped in container group `mycontainer`.</span></span> <span data-ttu-id="9d299-121">По умолчанию в журнале возвращается до 4 МБ.</span><span class="sxs-lookup"><span data-stu-id="9d299-121">By default, it will return up to 4MB log content.</span></span>

## <span data-ttu-id="9d299-122">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9d299-122">PARAMETERS</span></span>

### <span data-ttu-id="9d299-123">-ContainerGroupName</span><span class="sxs-lookup"><span data-stu-id="9d299-123">-ContainerGroupName</span></span>
<span data-ttu-id="9d299-124">Имя группы контейнеров.</span><span class="sxs-lookup"><span data-stu-id="9d299-124">The container group name.</span></span>

```yaml
Type: System.String
Parameter Sets: GetContainerInstanceLogByNamesParamSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9d299-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9d299-125">-DefaultProfile</span></span>
<span data-ttu-id="9d299-126">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="9d299-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9d299-127">-InputContainerGroup</span><span class="sxs-lookup"><span data-stu-id="9d299-127">-InputContainerGroup</span></span>
<span data-ttu-id="9d299-128">Объект группы контейнеров ввода.</span><span class="sxs-lookup"><span data-stu-id="9d299-128">The input container group object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ContainerInstance.Models.PSContainerGroup
Parameter Sets: GetContainerInstanceLogByPSContainerGroupParamSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9d299-129">-Name</span><span class="sxs-lookup"><span data-stu-id="9d299-129">-Name</span></span>
<span data-ttu-id="9d299-130">Имя экземпляра контейнера в группе контейнеров.</span><span class="sxs-lookup"><span data-stu-id="9d299-130">The container instance name in the container group.</span></span>
<span data-ttu-id="9d299-131">По умолчанию: то же самое, что и имя группы контейнера</span><span class="sxs-lookup"><span data-stu-id="9d299-131">Default: the same as the container group name</span></span>

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

### <span data-ttu-id="9d299-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9d299-132">-ResourceGroupName</span></span>
<span data-ttu-id="9d299-133">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="9d299-133">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: GetContainerInstanceLogByNamesParamSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9d299-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9d299-134">-ResourceId</span></span>
<span data-ttu-id="9d299-135">ИД ресурса.</span><span class="sxs-lookup"><span data-stu-id="9d299-135">The resource id.</span></span>

```yaml
Type: System.String
Parameter Sets: GetContainerInstanceLogByResourceIdParamSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9d299-136">-Tail</span><span class="sxs-lookup"><span data-stu-id="9d299-136">-Tail</span></span>
<span data-ttu-id="9d299-137">Количество строк в журнале.</span><span class="sxs-lookup"><span data-stu-id="9d299-137">The number of lines to tail the log.</span></span>
<span data-ttu-id="9d299-138">Если не указать, возвращается до 4 МБ в журнале с хвостами</span><span class="sxs-lookup"><span data-stu-id="9d299-138">If not specify, the cmdlet will return up to 4MB tailed log</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9d299-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9d299-139">CommonParameters</span></span>
<span data-ttu-id="9d299-140">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9d299-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9d299-141">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9d299-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9d299-142">INPUTS</span><span class="sxs-lookup"><span data-stu-id="9d299-142">INPUTS</span></span>

### <span data-ttu-id="9d299-143">Microsoft.Azure.Commands.ContainerInstance.Models.PSContainerGroup</span><span class="sxs-lookup"><span data-stu-id="9d299-143">Microsoft.Azure.Commands.ContainerInstance.Models.PSContainerGroup</span></span>

### <span data-ttu-id="9d299-144">System.String</span><span class="sxs-lookup"><span data-stu-id="9d299-144">System.String</span></span>

## <span data-ttu-id="9d299-145">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="9d299-145">OUTPUTS</span></span>

### <span data-ttu-id="9d299-146">System.String</span><span class="sxs-lookup"><span data-stu-id="9d299-146">System.String</span></span>

## <span data-ttu-id="9d299-147">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="9d299-147">NOTES</span></span>

## <span data-ttu-id="9d299-148">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="9d299-148">RELATED LINKS</span></span>
