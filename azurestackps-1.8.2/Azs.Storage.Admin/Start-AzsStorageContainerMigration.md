---
external help file: Azs.Storage.Admin-help.xml
Module Name: Azs.Storage.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: af9c5d2c5ebb547a6e09d2e4f4302ed2da470a39
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/08/2020
ms.locfileid: "94077054"
---
# <span data-ttu-id="f9379-101">Start-AzsStorageContainerMigration</span><span class="sxs-lookup"><span data-stu-id="f9379-101">Start-AzsStorageContainerMigration</span></span>

## <span data-ttu-id="f9379-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="f9379-102">SYNOPSIS</span></span>
<span data-ttu-id="f9379-103">Запускает задание миграции контейнера для миграции контейнеров в указанную конечную папку.</span><span class="sxs-lookup"><span data-stu-id="f9379-103">Starts a container migration job to migrate containers to the specified destination share.</span></span>

## <span data-ttu-id="f9379-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="f9379-104">SYNTAX</span></span>

```
Start-AzsStorageContainerMigration [-StorageAccountName] <String> [-ContainerName] <String>
 [-ShareName] <String> [[-ResourceGroupName] <String>] [-FarmName] <String> [-DestinationShareUncPath] <String>
 [-AsJob] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f9379-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f9379-105">DESCRIPTION</span></span>
<span data-ttu-id="f9379-106">Запускает задание миграции контейнера для миграции контейнеров в указанную конечную папку.</span><span class="sxs-lookup"><span data-stu-id="f9379-106">Starts a container migration job to migrate containers to the specified destination share.</span></span>

## <span data-ttu-id="f9379-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="f9379-107">EXAMPLES</span></span>

### <span data-ttu-id="f9379-108">ПРИМЕР 1</span><span class="sxs-lookup"><span data-stu-id="f9379-108">EXAMPLE 1</span></span>
```
Start-AzsStorageContainerMigration -StorageAccountName "accountTest" -ContainerName "containerTest" -ShareName "shareTest" -FarmName "10e8d576-d73c-454c-a40a-aee31a77a5f0" -DestinationShareUncPath "\\***.***.***.***\C$\Test"
```

<span data-ttu-id="f9379-109">Запускает миграцию контейнера.</span><span class="sxs-lookup"><span data-stu-id="f9379-109">Starts a container migration.</span></span>

## <span data-ttu-id="f9379-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="f9379-110">PARAMETERS</span></span>

### <span data-ttu-id="f9379-111">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="f9379-111">-StorageAccountName</span></span>
<span data-ttu-id="f9379-112">Имя учетной записи хранилища, в которой находится контейнер.</span><span class="sxs-lookup"><span data-stu-id="f9379-112">The name of storage account where the container locates.</span></span>

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

### <span data-ttu-id="f9379-113">-ContainerName</span><span class="sxs-lookup"><span data-stu-id="f9379-113">-ContainerName</span></span>
<span data-ttu-id="f9379-114">Имя контейнера для миграции.</span><span class="sxs-lookup"><span data-stu-id="f9379-114">The name of the container to be migrated.</span></span>

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

### <span data-ttu-id="f9379-115">-Имя_общего_ресурса</span><span class="sxs-lookup"><span data-stu-id="f9379-115">-ShareName</span></span>
<span data-ttu-id="f9379-116">Имя общего доступа, содержащего контейнер, указанный для миграции.</span><span class="sxs-lookup"><span data-stu-id="f9379-116">Name of the share containing the container specified for migration.</span></span>

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

### <span data-ttu-id="f9379-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f9379-117">-ResourceGroupName</span></span>
<span data-ttu-id="f9379-118">Имя группы ресурсов, в которой зарегистрирован поставщик ресурсов хранилища.</span><span class="sxs-lookup"><span data-stu-id="f9379-118">The resource group name in which the storage resource provider was registered under.</span></span>

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

### <span data-ttu-id="f9379-119">-FarmName</span><span class="sxs-lookup"><span data-stu-id="f9379-119">-FarmName</span></span>
<span data-ttu-id="f9379-120">Идентификатор фермы.</span><span class="sxs-lookup"><span data-stu-id="f9379-120">Farm Id.</span></span>

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

### <span data-ttu-id="f9379-121">-DestinationShareUncPath</span><span class="sxs-lookup"><span data-stu-id="f9379-121">-DestinationShareUncPath</span></span>
<span data-ttu-id="f9379-122">UNC-путь к целевой общей папке для миграции.</span><span class="sxs-lookup"><span data-stu-id="f9379-122">The UNC path of the destination share for migration.</span></span>

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

### <span data-ttu-id="f9379-123">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f9379-123">-AsJob</span></span>
<span data-ttu-id="f9379-124">Запустите асинхронно как задание и верните объект задания.</span><span class="sxs-lookup"><span data-stu-id="f9379-124">Run asynchronous as a job and return the job object.</span></span>

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

### <span data-ttu-id="f9379-125">-Force</span><span class="sxs-lookup"><span data-stu-id="f9379-125">-Force</span></span>
<span data-ttu-id="f9379-126">Не запрашивать подтверждение.</span><span class="sxs-lookup"><span data-stu-id="f9379-126">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="f9379-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f9379-127">-WhatIf</span></span>
<span data-ttu-id="f9379-128">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="f9379-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f9379-129">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="f9379-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f9379-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f9379-130">-Confirm</span></span>
<span data-ttu-id="f9379-131">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="f9379-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f9379-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f9379-132">CommonParameters</span></span>
<span data-ttu-id="f9379-133">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="f9379-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f9379-134">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f9379-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f9379-135">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="f9379-135">INPUTS</span></span>

## <span data-ttu-id="f9379-136">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="f9379-136">OUTPUTS</span></span>

## <span data-ttu-id="f9379-137">Пуск</span><span class="sxs-lookup"><span data-stu-id="f9379-137">NOTES</span></span>

## <span data-ttu-id="f9379-138">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f9379-138">RELATED LINKS</span></span>
