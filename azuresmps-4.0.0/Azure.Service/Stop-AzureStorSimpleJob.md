---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: A1E143A8-70F2-4158-9A10-F2082AD62A73
online version: ''
schema: 2.0.0
ms.openlocfilehash: 371291f4bd33809bc2f5880e4380c448219ed37a
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94076012"
---
# <span data-ttu-id="a8bce-101">Stop-AzureStorSimpleJob</span><span class="sxs-lookup"><span data-stu-id="a8bce-101">Stop-AzureStorSimpleJob</span></span>

## <span data-ttu-id="a8bce-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="a8bce-102">SYNOPSIS</span></span>
<span data-ttu-id="a8bce-103">Остановка задания StorSimple.</span><span class="sxs-lookup"><span data-stu-id="a8bce-103">Stops a StorSimple job.</span></span>

## <span data-ttu-id="a8bce-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="a8bce-104">SYNTAX</span></span>

```
Stop-AzureStorSimpleJob -InstanceId <String> [-Force] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="a8bce-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a8bce-105">DESCRIPTION</span></span>
<span data-ttu-id="a8bce-106">Командлет **Stop-AzureStorSimpleJob** останавливает выполнение задания StorSimple.</span><span class="sxs-lookup"><span data-stu-id="a8bce-106">The **Stop-AzureStorSimpleJob** cmdlet stops an on-going StorSimple job.</span></span>
<span data-ttu-id="a8bce-107">Вы можете указать задания, указав идентификатор экземпляра или имя задания.</span><span class="sxs-lookup"><span data-stu-id="a8bce-107">You can specify a jobs by supplying an instance ID or a job name.</span></span>

## <span data-ttu-id="a8bce-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="a8bce-108">EXAMPLES</span></span>

### <span data-ttu-id="a8bce-109">Пример 1: остановка заданий для устройства</span><span class="sxs-lookup"><span data-stu-id="a8bce-109">Example 1: Stop jobs for a device</span></span>
```
PS C:\>Get-AzureStorSimpleJob -DeviceName "Device07" | Stop-AzureStorSimpleJob -Force
```

<span data-ttu-id="a8bce-110">Эта команда получает задания для устройства с именем Device07 с помощью командлета **Get-AzureStorSimpleJob** .</span><span class="sxs-lookup"><span data-stu-id="a8bce-110">This command gets the jobs for the device named Device07, by using the **Get-AzureStorSimpleJob** cmdlet.</span></span>
<span data-ttu-id="a8bce-111">Команда передает задания в текущий командлет с помощью оператора конвейера.</span><span class="sxs-lookup"><span data-stu-id="a8bce-111">The command passes the jobs to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="a8bce-112">Текущий командлет останавливает все задания, передаваемые ей командой.</span><span class="sxs-lookup"><span data-stu-id="a8bce-112">The current cmdlet stops any jobs that the command passes to it.</span></span>
<span data-ttu-id="a8bce-113">Команда задает параметр *Force* и, таким образом, не запрашивает подтверждение перед тем, как остановить задание.</span><span class="sxs-lookup"><span data-stu-id="a8bce-113">The command specifies the *Force* parameter, and, so, it does not prompt you for confirmation before it stops a job.</span></span>

### <span data-ttu-id="a8bce-114">Пример 2: остановка определенного задания</span><span class="sxs-lookup"><span data-stu-id="a8bce-114">Example 2: Stop a specific job</span></span>
```
PS C:\>Stop-AzureStorSimpleJob -InstanceId "574f47e0-44e9-495c-b8a5-0203c57ebf6d" -Force
```

<span data-ttu-id="a8bce-115">Эта команда останавливает задание с указанным ИДЕНТИФИКАТОРом экземпляра.</span><span class="sxs-lookup"><span data-stu-id="a8bce-115">This command stops the job that has the specified instance ID.</span></span>

## <span data-ttu-id="a8bce-116">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="a8bce-116">PARAMETERS</span></span>

### <span data-ttu-id="a8bce-117">-Force</span><span class="sxs-lookup"><span data-stu-id="a8bce-117">-Force</span></span>
<span data-ttu-id="a8bce-118">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="a8bce-118">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="a8bce-119">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="a8bce-119">-InstanceId</span></span>
<span data-ttu-id="a8bce-120">Указывает ИД задания для устройства, которое нужно остановить.</span><span class="sxs-lookup"><span data-stu-id="a8bce-120">Specifies the ID of the device job to stop.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a8bce-121">-Profile</span><span class="sxs-lookup"><span data-stu-id="a8bce-121">-Profile</span></span>
<span data-ttu-id="a8bce-122">Указывает профиль Azure.</span><span class="sxs-lookup"><span data-stu-id="a8bce-122">Specifies an Azure profile.</span></span>

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

### <span data-ttu-id="a8bce-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a8bce-123">CommonParameters</span></span>
<span data-ttu-id="a8bce-124">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="a8bce-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a8bce-125">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a8bce-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a8bce-126">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="a8bce-126">INPUTS</span></span>

### <span data-ttu-id="a8bce-127">Ничего</span><span class="sxs-lookup"><span data-stu-id="a8bce-127">None</span></span>

## <span data-ttu-id="a8bce-128">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="a8bce-128">OUTPUTS</span></span>

### <span data-ttu-id="a8bce-129">DeviceJobDetails</span><span class="sxs-lookup"><span data-stu-id="a8bce-129">DeviceJobDetails</span></span>
<span data-ttu-id="a8bce-130">Этот командлет получает сведения о **DeviceJob** , который завершается этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="a8bce-130">This cmdlet gets details of the **DeviceJob** that this cmdlet stops.</span></span>

## <span data-ttu-id="a8bce-131">Пуск</span><span class="sxs-lookup"><span data-stu-id="a8bce-131">NOTES</span></span>

## <span data-ttu-id="a8bce-132">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a8bce-132">RELATED LINKS</span></span>

[<span data-ttu-id="a8bce-133">Get-AzureStorSimpleJob</span><span class="sxs-lookup"><span data-stu-id="a8bce-133">Get-AzureStorSimpleJob</span></span>](./Get-AzureStorSimpleJob.md)


