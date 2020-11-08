---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: C50959BB-7481-4898-BF4B-C5ABF8758473
online version: ''
schema: 2.0.0
ms.openlocfilehash: e2c06455004afbd15235f59164034abc2147964b
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94076453"
---
# <span data-ttu-id="77734-101">Remove-AzureStorSimpleDeviceVolumeContainer</span><span class="sxs-lookup"><span data-stu-id="77734-101">Remove-AzureStorSimpleDeviceVolumeContainer</span></span>

## <span data-ttu-id="77734-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="77734-102">SYNOPSIS</span></span>
<span data-ttu-id="77734-103">Удаление контейнера тома с устройства StorSimple.</span><span class="sxs-lookup"><span data-stu-id="77734-103">Removes a volume container from a StorSimple device.</span></span>

## <span data-ttu-id="77734-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="77734-104">SYNTAX</span></span>

```
Remove-AzureStorSimpleDeviceVolumeContainer -DeviceName <String> -VolumeContainer <DataContainer>
 [-WaitForComplete] [-Force] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="77734-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="77734-105">DESCRIPTION</span></span>
<span data-ttu-id="77734-106">Командлет **Remove-AzureStorSimpleDeviceVolumeContainer** удаляет объект контейнера тома на устройстве StorSimple.</span><span class="sxs-lookup"><span data-stu-id="77734-106">The **Remove-AzureStorSimpleDeviceVolumeContainer** cmdlet removes a volume container object from a StorSimple device.</span></span>
<span data-ttu-id="77734-107">Этот командлет запрашивает подтверждение, если не указан параметр *Force* .</span><span class="sxs-lookup"><span data-stu-id="77734-107">This cmdlet prompts you for confirmation unless you specify the *Force* parameter.</span></span>

## <span data-ttu-id="77734-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="77734-108">EXAMPLES</span></span>

### <span data-ttu-id="77734-109">Пример 1: удаление контейнера с помощью конвейера</span><span class="sxs-lookup"><span data-stu-id="77734-109">Example 1: Remove a container by using the pipeline</span></span>
```
PS C:\>Get-AzureStorSimpleDeviceVolumeContainer -DeviceName "Contoso63-AppVm" -VolumeContainerName "Container08" | Remove-AzureStorSimpleDeviceVolumeContainer -DeviceName "Contoso63-AppVm" -Force
VERBOSE: ClientRequestId: 0efbb4fc-ceb0-4311-bc49-0e08161d0a37_PS
VERBOSE: ClientRequestId: bf5b615f-47e3-4868-91b6-f2d12217a302_PS
VERBOSE: ClientRequestId: 5590c87e-0602-4197-b6c3-cf58b0e7a7b3_PS
VERBOSE: ClientRequestId: b33c71ac-c345-44ff-8213-d7fdf9f8480a_PS
VERBOSE: ClientRequestId: 903d42ef-58f4-4e89-ba7f-5f234262356d_PS
VERBOSE: About to create a job to remove your Volume container! 
VERBOSE: ClientRequestId: 2279575f-5115-4344-9c6f-9ef599bd203e_PS
e9ddec89-67ac-4e2e-a2ed-820de3547bb0
VERBOSE: The delete task is submitted successfully. Please use the command Get-AzureStorSimpleTask -InstanceId
e9ddec89-67ac-4e2e-a2ed-820de3547bb0 for tracking the task's status
VERBOSE: Volume container with name: Container08 is found.
```

<span data-ttu-id="77734-110">Эта команда получает контейнер томов с именем Container08 на устройстве с именем Contoso63-AppVm с помощью командлета **Get-AzureStorSimpleDeviceVolumeContainer** .</span><span class="sxs-lookup"><span data-stu-id="77734-110">This command gets the volume container named Container08 on the device named Contoso63-AppVm by using the **Get-AzureStorSimpleDeviceVolumeContainer** cmdlet.</span></span>
<span data-ttu-id="77734-111">Команда передает контейнер томов в текущий командлет с помощью оператора конвейера.</span><span class="sxs-lookup"><span data-stu-id="77734-111">The command passes the volume container to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="77734-112">Эта команда запускает задачу для удаления контейнера и возвращает объект **TaskResponse** .</span><span class="sxs-lookup"><span data-stu-id="77734-112">This command starts the task to remove the container, and then returns a **TaskResponse** object.</span></span>
<span data-ttu-id="77734-113">Чтобы просмотреть состояние задачи, используйте командлет **Get-AzureStorSimpleTask** .</span><span class="sxs-lookup"><span data-stu-id="77734-113">To see the status of the task, use the **Get-AzureStorSimpleTask** cmdlet.</span></span>
<span data-ttu-id="77734-114">Эта команда задает параметр *Force* , поэтому он не будет запрашивать подтверждение.</span><span class="sxs-lookup"><span data-stu-id="77734-114">This command specifies the *Force* parameter, so it does not prompt you for confirmation.</span></span>

## <span data-ttu-id="77734-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="77734-115">PARAMETERS</span></span>

### <span data-ttu-id="77734-116">-Имя_устройства</span><span class="sxs-lookup"><span data-stu-id="77734-116">-DeviceName</span></span>
<span data-ttu-id="77734-117">Указывает имя устройства StorSimple, на котором находится удаляемый контейнер тома.</span><span class="sxs-lookup"><span data-stu-id="77734-117">Specifies the name of the StorSimple device on which to the volume container to remove exists.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="77734-118">-Force</span><span class="sxs-lookup"><span data-stu-id="77734-118">-Force</span></span>
<span data-ttu-id="77734-119">Указывает на то, что этот командлет не запрашивает подтверждение.</span><span class="sxs-lookup"><span data-stu-id="77734-119">Indicates that this cmdlet does not prompt you for confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="77734-120">-Profile</span><span class="sxs-lookup"><span data-stu-id="77734-120">-Profile</span></span>
<span data-ttu-id="77734-121">Указывает профиль Azure.</span><span class="sxs-lookup"><span data-stu-id="77734-121">Specifies an Azure profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="77734-122">-VolumeContainer</span><span class="sxs-lookup"><span data-stu-id="77734-122">-VolumeContainer</span></span>
<span data-ttu-id="77734-123">Указывает контейнер томов, который нужно удалить, как объект **содержания** .</span><span class="sxs-lookup"><span data-stu-id="77734-123">Specifies the volume container to remove, as a **DataContainer** object.</span></span>
<span data-ttu-id="77734-124">Чтобы получить объект- **контейнер** , используйте командлет **Get-AzureStorSimpleDeviceVolumeContainer** .</span><span class="sxs-lookup"><span data-stu-id="77734-124">To obtain a **DataContainer** object, use the **Get-AzureStorSimpleDeviceVolumeContainer** cmdlet.</span></span>

```yaml
Type: DataContainer
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="77734-125">-WaitForComplete</span><span class="sxs-lookup"><span data-stu-id="77734-125">-WaitForComplete</span></span>
<span data-ttu-id="77734-126">Указывает на то, что этот командлет ожидает завершения операции до того, как она возвратит управление на консоль Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="77734-126">Indicates that this cmdlet waits for the operation to complete before it returns control to the Windows PowerShell console.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="77734-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="77734-127">CommonParameters</span></span>
<span data-ttu-id="77734-128">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="77734-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="77734-129">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="77734-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="77734-130">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="77734-130">INPUTS</span></span>

### <span data-ttu-id="77734-131">Контейнер содержания</span><span class="sxs-lookup"><span data-stu-id="77734-131">DataContainer</span></span>
<span data-ttu-id="77734-132">Этот командлет принимает объект- **контейнер** , который нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="77734-132">This cmdlet accepts a **DataContainer** object to remove.</span></span>

## <span data-ttu-id="77734-133">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="77734-133">OUTPUTS</span></span>

### <span data-ttu-id="77734-134">TaskStatusInfo</span><span class="sxs-lookup"><span data-stu-id="77734-134">TaskStatusInfo</span></span>
<span data-ttu-id="77734-135">Этот командлет возвращает объект **TaskStatusInfo** , если указан параметр *WaitForComplete* .</span><span class="sxs-lookup"><span data-stu-id="77734-135">This cmdlet returns a **TaskStatusInfo** object, if you specify the *WaitForComplete* parameter.</span></span>

## <span data-ttu-id="77734-136">Пуск</span><span class="sxs-lookup"><span data-stu-id="77734-136">NOTES</span></span>

## <span data-ttu-id="77734-137">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="77734-137">RELATED LINKS</span></span>

[<span data-ttu-id="77734-138">Get-AzureStorSimpleDeviceVolumeContainer</span><span class="sxs-lookup"><span data-stu-id="77734-138">Get-AzureStorSimpleDeviceVolumeContainer</span></span>](./Get-AzureStorSimpleDeviceVolumeContainer.md)

[<span data-ttu-id="77734-139">New-AzureStorSimpleDeviceVolumeContainer</span><span class="sxs-lookup"><span data-stu-id="77734-139">New-AzureStorSimpleDeviceVolumeContainer</span></span>](./New-AzureStorSimpleDeviceVolumeContainer.md)


