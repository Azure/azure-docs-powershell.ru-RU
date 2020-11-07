---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerInstance.dll-Help.xml
Module Name: Az.ContainerInstance
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerinstance/get-azcontainerinstancelog
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerInstance/ContainerInstance/help/Get-AzContainerInstanceLog.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerInstance/ContainerInstance/help/Get-AzContainerInstanceLog.md
ms.openlocfilehash: f046b9a57f0827977927e31d5009c6276cd89279
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93721611"
---
# <span data-ttu-id="dd7a4-101">Get-AzContainerInstanceLog</span><span class="sxs-lookup"><span data-stu-id="dd7a4-101">Get-AzContainerInstanceLog</span></span>

## <span data-ttu-id="dd7a4-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="dd7a4-102">SYNOPSIS</span></span>
<span data-ttu-id="dd7a4-103">Получение журналов экземпляра контейнера в группе контейнера.</span><span class="sxs-lookup"><span data-stu-id="dd7a4-103">Get the logs of a container instance in a container group.</span></span>

## <span data-ttu-id="dd7a4-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="dd7a4-104">SYNTAX</span></span>

### <span data-ttu-id="dd7a4-105">GetContainerInstanceLogByNamesParamSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="dd7a4-105">GetContainerInstanceLogByNamesParamSet (Default)</span></span>
```
Get-AzContainerInstanceLog [-ResourceGroupName] <String> -ContainerGroupName <String> [-Name <String>]
 [-Tail <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="dd7a4-106">GetContainerInstanceLogByPSContainerGroupParamSet</span><span class="sxs-lookup"><span data-stu-id="dd7a4-106">GetContainerInstanceLogByPSContainerGroupParamSet</span></span>
```
Get-AzContainerInstanceLog -InputContainerGroup <PSContainerGroup> [-Name <String>] [-Tail <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="dd7a4-107">GetContainerInstanceLogByResourceIdParamSet</span><span class="sxs-lookup"><span data-stu-id="dd7a4-107">GetContainerInstanceLogByResourceIdParamSet</span></span>
```
Get-AzContainerInstanceLog -ResourceId <String> [-Name <String>] [-Tail <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="dd7a4-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="dd7a4-108">DESCRIPTION</span></span>
<span data-ttu-id="dd7a4-109">Командлет **Get-AzContainerInstanceLog** получает журналы контейнера в группе контейнера.</span><span class="sxs-lookup"><span data-stu-id="dd7a4-109">The **Get-AzContainerInstanceLog** cmdlet gets the logs of a container in a container group.</span></span>

## <span data-ttu-id="dd7a4-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="dd7a4-110">EXAMPLES</span></span>

### <span data-ttu-id="dd7a4-111">Пример 1: получение журнала хвоста экземпляра контейнера</span><span class="sxs-lookup"><span data-stu-id="dd7a4-111">Example 1: Get the tail log of a container instance</span></span>
```
PS C:\> Get-AzContainerInstanceLog -ResourceGroupName demo -ContainerGroupName mycontainer -Name container1

Log line 1.
Log line 2.
Log line 3.
Log line 4.
```

<span data-ttu-id="dd7a4-112">Получение журнала из `container1` группы "контейнер" `mycontainer` .</span><span class="sxs-lookup"><span data-stu-id="dd7a4-112">Get the log from `container1` in container group `mycontainer`.</span></span> <span data-ttu-id="dd7a4-113">По умолчанию будет возвращено не более 4 МБАЙТ содержимого журнала.</span><span class="sxs-lookup"><span data-stu-id="dd7a4-113">By default, it will return up to 4MB log content.</span></span>

### <span data-ttu-id="dd7a4-114">Пример 2: получение журнала заключительного фрагмента для экземпляра контейнера с тем же именем, что и группа "контейнер"</span><span class="sxs-lookup"><span data-stu-id="dd7a4-114">Example 2: Get the tail log of a container instance that has the same name as the container group</span></span>
```
PS C:\> Get-AzContainerInstanceLog -ResourceGroupName demo -ContainerGroupName mycontainer

Log line 1.
Log line 2.
Log line 3.
Log line 4.
```

<span data-ttu-id="dd7a4-115">Получение журнала из `mycontainer` группы "контейнер" `mycontainer` .</span><span class="sxs-lookup"><span data-stu-id="dd7a4-115">Get the log from `mycontainer` in container group `mycontainer`.</span></span> <span data-ttu-id="dd7a4-116">По умолчанию будет возвращено не более 4 МБАЙТ содержимого журнала.</span><span class="sxs-lookup"><span data-stu-id="dd7a4-116">By default, it will return up to 4MB log content.</span></span>

### <span data-ttu-id="dd7a4-117">Пример 3: получение строк с хвостовиком 2 журнала экземпляра контейнера</span><span class="sxs-lookup"><span data-stu-id="dd7a4-117">Example 3: Get the tail 2 lines of log of a container instance</span></span>
```
PS C:\> Get-AzContainerInstanceLog -ResourceGroupName demo -ContainerGroupName mycontainer -Name container1 -Tail 2

Log line 3.
Log line 4.
```

<span data-ttu-id="dd7a4-118">Получение строк с хвостовиком 2 из журнала `container1` в группе "контейнер" `mycontainer` .</span><span class="sxs-lookup"><span data-stu-id="dd7a4-118">Get the tail 2 lines of log from `container1` in container group `mycontainer`.</span></span>

### <span data-ttu-id="dd7a4-119">Пример 4: получение журнала заключительного фрагмента для экземпляра контейнера в переданном элементе Group Container</span><span class="sxs-lookup"><span data-stu-id="dd7a4-119">Example 4: Get the tail log of a container instance in a piped in container group</span></span>
```
PS C:\> Get-AzContainerGroup -ResourceGroupName demo -Name mycontainer | Get-AzContainerInstanceLog

Log line 1.
Log line 2.
Log line 3.
Log line 4.
```

<span data-ttu-id="dd7a4-120">Получение журнала из группы в списке "передаваться" `mycontainer` в группе "контейнер" `mycontainer` .</span><span class="sxs-lookup"><span data-stu-id="dd7a4-120">Get the log from `mycontainer` in piped in container group `mycontainer`.</span></span> <span data-ttu-id="dd7a4-121">По умолчанию будет возвращено не более 4 МБАЙТ содержимого журнала.</span><span class="sxs-lookup"><span data-stu-id="dd7a4-121">By default, it will return up to 4MB log content.</span></span>

## <span data-ttu-id="dd7a4-122">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="dd7a4-122">PARAMETERS</span></span>

### <span data-ttu-id="dd7a4-123">-ContainerGroupName</span><span class="sxs-lookup"><span data-stu-id="dd7a4-123">-ContainerGroupName</span></span>
<span data-ttu-id="dd7a4-124">Имя группы контейнера.</span><span class="sxs-lookup"><span data-stu-id="dd7a4-124">The container group name.</span></span>

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

### <span data-ttu-id="dd7a4-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dd7a4-125">-DefaultProfile</span></span>
<span data-ttu-id="dd7a4-126">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="dd7a4-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="dd7a4-127">-InputContainerGroup</span><span class="sxs-lookup"><span data-stu-id="dd7a4-127">-InputContainerGroup</span></span>
<span data-ttu-id="dd7a4-128">Объект группы контейнера входных данных.</span><span class="sxs-lookup"><span data-stu-id="dd7a4-128">The input container group object.</span></span>

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

### <span data-ttu-id="dd7a4-129">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="dd7a4-129">-Name</span></span>
<span data-ttu-id="dd7a4-130">Имя контейнера в группе "контейнер".</span><span class="sxs-lookup"><span data-stu-id="dd7a4-130">The container instance name in the container group.</span></span>
<span data-ttu-id="dd7a4-131">По умолчанию: то же, что и имя группы контейнера</span><span class="sxs-lookup"><span data-stu-id="dd7a4-131">Default: the same as the container group name</span></span>

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

### <span data-ttu-id="dd7a4-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dd7a4-132">-ResourceGroupName</span></span>
<span data-ttu-id="dd7a4-133">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="dd7a4-133">The resource group name.</span></span>

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

### <span data-ttu-id="dd7a4-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="dd7a4-134">-ResourceId</span></span>
<span data-ttu-id="dd7a4-135">Идентификатор ресурса.</span><span class="sxs-lookup"><span data-stu-id="dd7a4-135">The resource id.</span></span>

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

### <span data-ttu-id="dd7a4-136">-Tail</span><span class="sxs-lookup"><span data-stu-id="dd7a4-136">-Tail</span></span>
<span data-ttu-id="dd7a4-137">Количество строк, которые нужно присвоить журналу.</span><span class="sxs-lookup"><span data-stu-id="dd7a4-137">The number of lines to tail the log.</span></span>
<span data-ttu-id="dd7a4-138">Если не указано, командлет вернется на заключительный логарифм с хвостовиком</span><span class="sxs-lookup"><span data-stu-id="dd7a4-138">If not specify, the cmdlet will return up to 4MB tailed log</span></span>

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

### <span data-ttu-id="dd7a4-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dd7a4-139">CommonParameters</span></span>
<span data-ttu-id="dd7a4-140">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="dd7a4-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dd7a4-141">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dd7a4-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dd7a4-142">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="dd7a4-142">INPUTS</span></span>

### <span data-ttu-id="dd7a4-143">Microsoft. Azure. Commands. ContainerInstance. Models. PSContainerGroup</span><span class="sxs-lookup"><span data-stu-id="dd7a4-143">Microsoft.Azure.Commands.ContainerInstance.Models.PSContainerGroup</span></span>

### <span data-ttu-id="dd7a4-144">System. String</span><span class="sxs-lookup"><span data-stu-id="dd7a4-144">System.String</span></span>

## <span data-ttu-id="dd7a4-145">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="dd7a4-145">OUTPUTS</span></span>

### <span data-ttu-id="dd7a4-146">System. String</span><span class="sxs-lookup"><span data-stu-id="dd7a4-146">System.String</span></span>

## <span data-ttu-id="dd7a4-147">Пуск</span><span class="sxs-lookup"><span data-stu-id="dd7a4-147">NOTES</span></span>

## <span data-ttu-id="dd7a4-148">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="dd7a4-148">RELATED LINKS</span></span>
