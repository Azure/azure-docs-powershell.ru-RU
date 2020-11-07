---
external help file: Azs.Storage.Admin-help.xml
Module Name: Azs.Storage.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 54016a200b4304c7e37777202a8450fc9ad10e1e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93720297"
---
# <span data-ttu-id="95d2e-101">Start-AzsStorageContainerMigration</span><span class="sxs-lookup"><span data-stu-id="95d2e-101">Start-AzsStorageContainerMigration</span></span>

## <span data-ttu-id="95d2e-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="95d2e-102">SYNOPSIS</span></span>
<span data-ttu-id="95d2e-103">Запускает задание миграции контейнера для миграции контейнеров в указанную конечную папку.</span><span class="sxs-lookup"><span data-stu-id="95d2e-103">Starts a container migration job to migrate containers to the specified destination share.</span></span>

## <span data-ttu-id="95d2e-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="95d2e-104">SYNTAX</span></span>

```
Start-AzsStorageContainerMigration [-StorageAccountName] <String> [-Name] <String> [-ShareName] <String>
 [[-ResourceGroupName] <String>] [-FarmName] <String> [-DestinationShareUncPath] <String> [-AsJob] [-Force]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="95d2e-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="95d2e-105">DESCRIPTION</span></span>
<span data-ttu-id="95d2e-106">Запускает задание миграции контейнера для миграции контейнеров в указанную конечную папку.</span><span class="sxs-lookup"><span data-stu-id="95d2e-106">Starts a container migration job to migrate containers to the specified destination share.</span></span>

## <span data-ttu-id="95d2e-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="95d2e-107">EXAMPLES</span></span>

### <span data-ttu-id="95d2e-108">--------------------------ПРИМЕР 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="95d2e-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Start-AzsStorageContainerMigration -StorageAccountName "accountTest" -Name "containerTest" -ShareName "shareTest" -FarmName "10e8d576-d73c-454c-a40a-aee31a77a5f0" -DestinationShareUncPath "\\***.***.***.***\C$\Test"
```

<span data-ttu-id="95d2e-109">Запускает миграцию контейнера.</span><span class="sxs-lookup"><span data-stu-id="95d2e-109">Starts a container migration.</span></span>

## <span data-ttu-id="95d2e-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="95d2e-110">PARAMETERS</span></span>

### <span data-ttu-id="95d2e-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="95d2e-111">-AsJob</span></span>
<span data-ttu-id="95d2e-112">Запустите асинхронно как задание и верните объект задания.</span><span class="sxs-lookup"><span data-stu-id="95d2e-112">Run asynchronous as a job and return the job object.</span></span>

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

### <span data-ttu-id="95d2e-113">-DestinationShareUncPath</span><span class="sxs-lookup"><span data-stu-id="95d2e-113">-DestinationShareUncPath</span></span>
<span data-ttu-id="95d2e-114">UNC-путь к целевой общей папке для миграции.</span><span class="sxs-lookup"><span data-stu-id="95d2e-114">The UNC path of the destination share for migration.</span></span>

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

### <span data-ttu-id="95d2e-115">-FarmName</span><span class="sxs-lookup"><span data-stu-id="95d2e-115">-FarmName</span></span>
<span data-ttu-id="95d2e-116">Идентификатор фермы.</span><span class="sxs-lookup"><span data-stu-id="95d2e-116">Farm Id.</span></span>

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

### <span data-ttu-id="95d2e-117">-Force</span><span class="sxs-lookup"><span data-stu-id="95d2e-117">-Force</span></span>
<span data-ttu-id="95d2e-118">Не запрашивать подтверждение.</span><span class="sxs-lookup"><span data-stu-id="95d2e-118">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="95d2e-119">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="95d2e-119">-Name</span></span>
<span data-ttu-id="95d2e-120">Имя контейнера для миграции.</span><span class="sxs-lookup"><span data-stu-id="95d2e-120">The name of the container to be migrated.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ContainerName

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="95d2e-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="95d2e-121">-ResourceGroupName</span></span>
<span data-ttu-id="95d2e-122">Имя группы ресурсов, в которой зарегистрирован поставщик ресурсов хранилища.</span><span class="sxs-lookup"><span data-stu-id="95d2e-122">The resource group name in which the storage resource provider was registered under.</span></span>

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

### <span data-ttu-id="95d2e-123">-Имя_общего_ресурса</span><span class="sxs-lookup"><span data-stu-id="95d2e-123">-ShareName</span></span>
<span data-ttu-id="95d2e-124">Имя общего доступа, содержащего контейнер, указанный для миграции.</span><span class="sxs-lookup"><span data-stu-id="95d2e-124">Name of the share containing the container specified for migration.</span></span>

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

### <span data-ttu-id="95d2e-125">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="95d2e-125">-StorageAccountName</span></span>
<span data-ttu-id="95d2e-126">Имя учетной записи хранилища, в которой находится контейнер.</span><span class="sxs-lookup"><span data-stu-id="95d2e-126">The name of storage account where the container locates.</span></span>

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

### <span data-ttu-id="95d2e-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="95d2e-127">-Confirm</span></span>
<span data-ttu-id="95d2e-128">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="95d2e-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="95d2e-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="95d2e-129">-WhatIf</span></span>
<span data-ttu-id="95d2e-130">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="95d2e-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="95d2e-131">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="95d2e-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="95d2e-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="95d2e-132">CommonParameters</span></span>
<span data-ttu-id="95d2e-133">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="95d2e-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="95d2e-134">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="95d2e-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="95d2e-135">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="95d2e-135">INPUTS</span></span>

## <span data-ttu-id="95d2e-136">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="95d2e-136">OUTPUTS</span></span>

## <span data-ttu-id="95d2e-137">Пуск</span><span class="sxs-lookup"><span data-stu-id="95d2e-137">NOTES</span></span>

## <span data-ttu-id="95d2e-138">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="95d2e-138">RELATED LINKS</span></span>

