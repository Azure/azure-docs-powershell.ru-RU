---
external help file: Azs.Storage.Admin-help.xml
Module Name: Azs.Storage.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: af9c5d2c5ebb547a6e09d2e4f4302ed2da470a39
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2020
ms.locfileid: "93908949"
---
# <span data-ttu-id="309ec-101">Start-AzsStorageContainerMigration</span><span class="sxs-lookup"><span data-stu-id="309ec-101">Start-AzsStorageContainerMigration</span></span>

## <span data-ttu-id="309ec-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="309ec-102">SYNOPSIS</span></span>
<span data-ttu-id="309ec-103">Запускает задание миграции контейнера для миграции контейнеров в указанную конечную папку.</span><span class="sxs-lookup"><span data-stu-id="309ec-103">Starts a container migration job to migrate containers to the specified destination share.</span></span>

## <span data-ttu-id="309ec-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="309ec-104">SYNTAX</span></span>

```
Start-AzsStorageContainerMigration [-StorageAccountName] <String> [-ContainerName] <String>
 [-ShareName] <String> [[-ResourceGroupName] <String>] [-FarmName] <String> [-DestinationShareUncPath] <String>
 [-AsJob] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="309ec-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="309ec-105">DESCRIPTION</span></span>
<span data-ttu-id="309ec-106">Запускает задание миграции контейнера для миграции контейнеров в указанную конечную папку.</span><span class="sxs-lookup"><span data-stu-id="309ec-106">Starts a container migration job to migrate containers to the specified destination share.</span></span>

## <span data-ttu-id="309ec-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="309ec-107">EXAMPLES</span></span>

### <span data-ttu-id="309ec-108">ПРИМЕР 1</span><span class="sxs-lookup"><span data-stu-id="309ec-108">EXAMPLE 1</span></span>
```
Start-AzsStorageContainerMigration -StorageAccountName "accountTest" -ContainerName "containerTest" -ShareName "shareTest" -FarmName "10e8d576-d73c-454c-a40a-aee31a77a5f0" -DestinationShareUncPath "\\***.***.***.***\C$\Test"
```

<span data-ttu-id="309ec-109">Запускает миграцию контейнера.</span><span class="sxs-lookup"><span data-stu-id="309ec-109">Starts a container migration.</span></span>

## <span data-ttu-id="309ec-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="309ec-110">PARAMETERS</span></span>

### <span data-ttu-id="309ec-111">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="309ec-111">-StorageAccountName</span></span>
<span data-ttu-id="309ec-112">Имя учетной записи хранилища, в которой находится контейнер.</span><span class="sxs-lookup"><span data-stu-id="309ec-112">The name of storage account where the container locates.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="309ec-113">-ContainerName</span><span class="sxs-lookup"><span data-stu-id="309ec-113">-ContainerName</span></span>
<span data-ttu-id="309ec-114">Имя контейнера для миграции.</span><span class="sxs-lookup"><span data-stu-id="309ec-114">The name of the container to be migrated.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="309ec-115">-Имя_общего_ресурса</span><span class="sxs-lookup"><span data-stu-id="309ec-115">-ShareName</span></span>
<span data-ttu-id="309ec-116">Имя общего доступа, содержащего контейнер, указанный для миграции.</span><span class="sxs-lookup"><span data-stu-id="309ec-116">Name of the share containing the container specified for migration.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="309ec-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="309ec-117">-ResourceGroupName</span></span>
<span data-ttu-id="309ec-118">Имя группы ресурсов, в которой зарегистрирован поставщик ресурсов хранилища.</span><span class="sxs-lookup"><span data-stu-id="309ec-118">The resource group name in which the storage resource provider was registered under.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="309ec-119">-FarmName</span><span class="sxs-lookup"><span data-stu-id="309ec-119">-FarmName</span></span>
<span data-ttu-id="309ec-120">Идентификатор фермы.</span><span class="sxs-lookup"><span data-stu-id="309ec-120">Farm Id.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="309ec-121">-DestinationShareUncPath</span><span class="sxs-lookup"><span data-stu-id="309ec-121">-DestinationShareUncPath</span></span>
<span data-ttu-id="309ec-122">UNC-путь к целевой общей папке для миграции.</span><span class="sxs-lookup"><span data-stu-id="309ec-122">The UNC path of the destination share for migration.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="309ec-123">-AsJob</span><span class="sxs-lookup"><span data-stu-id="309ec-123">-AsJob</span></span>
<span data-ttu-id="309ec-124">Запустите асинхронно как задание и верните объект задания.</span><span class="sxs-lookup"><span data-stu-id="309ec-124">Run asynchronous as a job and return the job object.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="309ec-125">-Force</span><span class="sxs-lookup"><span data-stu-id="309ec-125">-Force</span></span>
<span data-ttu-id="309ec-126">Не запрашивать подтверждение.</span><span class="sxs-lookup"><span data-stu-id="309ec-126">Do not ask for confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="309ec-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="309ec-127">-WhatIf</span></span>
<span data-ttu-id="309ec-128">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="309ec-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="309ec-129">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="309ec-129">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="309ec-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="309ec-130">-Confirm</span></span>
<span data-ttu-id="309ec-131">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="309ec-131">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="309ec-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="309ec-132">CommonParameters</span></span>
<span data-ttu-id="309ec-133">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="309ec-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="309ec-134">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="309ec-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="309ec-135">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="309ec-135">INPUTS</span></span>

## <span data-ttu-id="309ec-136">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="309ec-136">OUTPUTS</span></span>

## <span data-ttu-id="309ec-137">Пуск</span><span class="sxs-lookup"><span data-stu-id="309ec-137">NOTES</span></span>

## <span data-ttu-id="309ec-138">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="309ec-138">RELATED LINKS</span></span>
