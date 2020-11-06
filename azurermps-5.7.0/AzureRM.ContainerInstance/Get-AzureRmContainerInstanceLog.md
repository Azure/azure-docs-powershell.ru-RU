---
external help file: Microsoft.Azure.Commands.ContainerInstance.dll-Help.xml
Module Name: AzureRM.ContainerInstance
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.containerinstance/get-azurermcontainerinstancelog
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerInstance/Commands.ContainerInstance/help/Get-AzureRmContainerInstanceLog.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerInstance/Commands.ContainerInstance/help/Get-AzureRmContainerInstanceLog.md
ms.openlocfilehash: 346973683ca7e360c4b4d63a4f2ed4f4856a0797
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93557451"
---
# <span data-ttu-id="a0a41-101">Get-AzureRmContainerInstanceLog</span><span class="sxs-lookup"><span data-stu-id="a0a41-101">Get-AzureRmContainerInstanceLog</span></span>

## <span data-ttu-id="a0a41-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="a0a41-102">SYNOPSIS</span></span>
<span data-ttu-id="a0a41-103">Получение журналов экземпляра контейнера в группе контейнера.</span><span class="sxs-lookup"><span data-stu-id="a0a41-103">Get the logs of a container instance in a container group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a0a41-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="a0a41-104">SYNTAX</span></span>

### <span data-ttu-id="a0a41-105">GetContainerInstanceLogByNamesParamSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="a0a41-105">GetContainerInstanceLogByNamesParamSet (Default)</span></span>
```
Get-AzureRmContainerInstanceLog [-ResourceGroupName] <String> -ContainerGroupName <String> [-Name <String>]
 [-Tail <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a0a41-106">GetContainerInstanceLogByPSContainerGroupParamSet</span><span class="sxs-lookup"><span data-stu-id="a0a41-106">GetContainerInstanceLogByPSContainerGroupParamSet</span></span>
```
Get-AzureRmContainerInstanceLog -InputContainerGroup <PSContainerGroup> [-Name <String>] [-Tail <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a0a41-107">GetContainerInstanceLogByResourceIdParamSet</span><span class="sxs-lookup"><span data-stu-id="a0a41-107">GetContainerInstanceLogByResourceIdParamSet</span></span>
```
Get-AzureRmContainerInstanceLog -ResourceId <String> [-Name <String>] [-Tail <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a0a41-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a0a41-108">DESCRIPTION</span></span>
<span data-ttu-id="a0a41-109">Командлет **Get-AzureRmContainerInstanceLog** получает журналы контейнера в группе контейнера.</span><span class="sxs-lookup"><span data-stu-id="a0a41-109">The **Get-AzureRmContainerInstanceLog** cmdlet gets the logs of a container in a container group.</span></span>

## <span data-ttu-id="a0a41-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="a0a41-110">EXAMPLES</span></span>

### <span data-ttu-id="a0a41-111">Пример 1: получение журнала хвоста экземпляра контейнера</span><span class="sxs-lookup"><span data-stu-id="a0a41-111">Example 1: Get the tail log of a container instance</span></span>
```
PS C:\> Get-AzureRmContainerInstanceLog -ResourceGroupName demo -ContainerGroupName mycontainer -Name container1

Log line 1.
Log line 2.
Log line 3.
Log line 4.
```

<span data-ttu-id="a0a41-112">Получение журнала из `container1` группы "контейнер" `mycontainer` .</span><span class="sxs-lookup"><span data-stu-id="a0a41-112">Get the log from `container1` in container group `mycontainer`.</span></span> <span data-ttu-id="a0a41-113">По умолчанию будет возвращено не более 4 МБАЙТ содержимого журнала.</span><span class="sxs-lookup"><span data-stu-id="a0a41-113">By default, it will return up to 4MB log content.</span></span>

### <span data-ttu-id="a0a41-114">Пример 2: получение журнала заключительного фрагмента для экземпляра контейнера с тем же именем, что и группа "контейнер"</span><span class="sxs-lookup"><span data-stu-id="a0a41-114">Example 2: Get the tail log of a container instance that has the same name as the container group</span></span>
```
PS C:\> Get-AzureRmContainerInstanceLog -ResourceGroupName demo -ContainerGroupName mycontainer

Log line 1.
Log line 2.
Log line 3.
Log line 4.
```

<span data-ttu-id="a0a41-115">Получение журнала из `mycontainer` группы "контейнер" `mycontainer` .</span><span class="sxs-lookup"><span data-stu-id="a0a41-115">Get the log from `mycontainer` in container group `mycontainer`.</span></span> <span data-ttu-id="a0a41-116">По умолчанию будет возвращено не более 4 МБАЙТ содержимого журнала.</span><span class="sxs-lookup"><span data-stu-id="a0a41-116">By default, it will return up to 4MB log content.</span></span>

### <span data-ttu-id="a0a41-117">Пример 3: получение строк с хвостовиком 2 журнала экземпляра контейнера</span><span class="sxs-lookup"><span data-stu-id="a0a41-117">Example 3: Get the tail 2 lines of log of a container instance</span></span>
```
PS C:\> Get-AzureRmContainerInstanceLog -ResourceGroupName demo -ContainerGroupName mycontainer -Name container1 -Tail 2

Log line 3.
Log line 4.
```

<span data-ttu-id="a0a41-118">Получение строк с хвостовиком 2 из журнала `container1` в группе "контейнер" `mycontainer` .</span><span class="sxs-lookup"><span data-stu-id="a0a41-118">Get the tail 2 lines of log from `container1` in container group `mycontainer`.</span></span>

### <span data-ttu-id="a0a41-119">Пример 4: получение журнала заключительного фрагмента для экземпляра контейнера в переданном элементе Group Container</span><span class="sxs-lookup"><span data-stu-id="a0a41-119">Example 4: Get the tail log of a container instance in a piped in container group</span></span>
```
PS C:\> Get-AzureRmContainerGroup -ResourceGroupName demo -Name mycontainer | Get-AzureRmContainerInstanceLog

Log line 1.
Log line 2.
Log line 3.
Log line 4.
```

<span data-ttu-id="a0a41-120">Получение журнала из группы в списке "передаваться" `mycontainer` в группе "контейнер" `mycontainer` .</span><span class="sxs-lookup"><span data-stu-id="a0a41-120">Get the log from `mycontainer` in piped in container group `mycontainer`.</span></span> <span data-ttu-id="a0a41-121">По умолчанию будет возвращено не более 4 МБАЙТ содержимого журнала.</span><span class="sxs-lookup"><span data-stu-id="a0a41-121">By default, it will return up to 4MB log content.</span></span>

## <span data-ttu-id="a0a41-122">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="a0a41-122">PARAMETERS</span></span>

### <span data-ttu-id="a0a41-123">-ContainerGroupName</span><span class="sxs-lookup"><span data-stu-id="a0a41-123">-ContainerGroupName</span></span>
<span data-ttu-id="a0a41-124">Имя группы контейнера.</span><span class="sxs-lookup"><span data-stu-id="a0a41-124">The container group name.</span></span>

```yaml
Type: String
Parameter Sets: GetContainerInstanceLogByNamesParamSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a0a41-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a0a41-125">-DefaultProfile</span></span>
<span data-ttu-id="a0a41-126">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="a0a41-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a0a41-127">-InputContainerGroup</span><span class="sxs-lookup"><span data-stu-id="a0a41-127">-InputContainerGroup</span></span>
<span data-ttu-id="a0a41-128">Объект группы контейнера входных данных.</span><span class="sxs-lookup"><span data-stu-id="a0a41-128">The input container group object.</span></span>

```yaml
Type: PSContainerGroup
Parameter Sets: GetContainerInstanceLogByPSContainerGroupParamSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a0a41-129">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="a0a41-129">-Name</span></span>
<span data-ttu-id="a0a41-130">Имя контейнера в группе "контейнер".</span><span class="sxs-lookup"><span data-stu-id="a0a41-130">The container instance name in the container group.</span></span>
<span data-ttu-id="a0a41-131">По умолчанию: то же, что и имя группы контейнера</span><span class="sxs-lookup"><span data-stu-id="a0a41-131">Default: the same as the container group name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a0a41-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a0a41-132">-ResourceGroupName</span></span>
<span data-ttu-id="a0a41-133">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="a0a41-133">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: GetContainerInstanceLogByNamesParamSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a0a41-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a0a41-134">-ResourceId</span></span>
<span data-ttu-id="a0a41-135">Идентификатор ресурса.</span><span class="sxs-lookup"><span data-stu-id="a0a41-135">The resource id.</span></span>

```yaml
Type: String
Parameter Sets: GetContainerInstanceLogByResourceIdParamSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a0a41-136">-Tail</span><span class="sxs-lookup"><span data-stu-id="a0a41-136">-Tail</span></span>
<span data-ttu-id="a0a41-137">Количество строк, которые нужно присвоить журналу.</span><span class="sxs-lookup"><span data-stu-id="a0a41-137">The number of lines to tail the log.</span></span>
<span data-ttu-id="a0a41-138">Если не указано, командлет вернется на заключительный логарифм с хвостовиком</span><span class="sxs-lookup"><span data-stu-id="a0a41-138">If not specify, the cmdlet will return up to 4MB tailed log</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a0a41-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a0a41-139">CommonParameters</span></span>
<span data-ttu-id="a0a41-140">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="a0a41-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a0a41-141">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a0a41-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a0a41-142">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="a0a41-142">INPUTS</span></span>

### <span data-ttu-id="a0a41-143">Microsoft. Azure. Commands. ContainerInstance. Models. PSContainerGroup</span><span class="sxs-lookup"><span data-stu-id="a0a41-143">Microsoft.Azure.Commands.ContainerInstance.Models.PSContainerGroup</span></span>

## <span data-ttu-id="a0a41-144">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="a0a41-144">OUTPUTS</span></span>

### <span data-ttu-id="a0a41-145">System. String</span><span class="sxs-lookup"><span data-stu-id="a0a41-145">System.String</span></span>

## <span data-ttu-id="a0a41-146">Пуск</span><span class="sxs-lookup"><span data-stu-id="a0a41-146">NOTES</span></span>

## <span data-ttu-id="a0a41-147">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a0a41-147">RELATED LINKS</span></span>
