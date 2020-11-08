---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: C60F78AE-3803-4D9F-A4F3-EAA42052C0E4
online version: ''
schema: 2.0.0
ms.openlocfilehash: 6a0708ca37cdb2b700772da2fe9cb684b8b29a30
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94075771"
---
# <span data-ttu-id="aee58-101">Start-AzureVM</span><span class="sxs-lookup"><span data-stu-id="aee58-101">Start-AzureVM</span></span>

## <span data-ttu-id="aee58-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="aee58-102">SYNOPSIS</span></span>
<span data-ttu-id="aee58-103">Запуск виртуальной машины Azure.</span><span class="sxs-lookup"><span data-stu-id="aee58-103">Starts an Azure virtual machine.</span></span>

## <span data-ttu-id="aee58-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="aee58-104">SYNTAX</span></span>

### <span data-ttu-id="aee58-105">ByName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="aee58-105">ByName (Default)</span></span>
```
Start-AzureVM [-Name] <String[]> [-ServiceName] <String> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="aee58-106">Вводим</span><span class="sxs-lookup"><span data-stu-id="aee58-106">Input</span></span>
```
Start-AzureVM -VM <IPersistentVM[]> [-ServiceName] <String> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="aee58-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="aee58-107">DESCRIPTION</span></span>
<span data-ttu-id="aee58-108">Командлет **Start-AzureVM** запрашивает начало виртуальной машины Azure.</span><span class="sxs-lookup"><span data-stu-id="aee58-108">The **Start-AzureVM** cmdlet requests the start of an Azure virtual machine.</span></span>

## <span data-ttu-id="aee58-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="aee58-109">EXAMPLES</span></span>

### <span data-ttu-id="aee58-110">Пример 1: Запуск виртуальной машины</span><span class="sxs-lookup"><span data-stu-id="aee58-110">Example 1: Start a virtual machine</span></span>
```
PS C:\> Start-AzureVM -ServiceName "ContosoService03" -Name "VirtualMachine04"
```

<span data-ttu-id="aee58-111">Эта команда запускает виртуальную машину с именем VirtualMachine04, которая выполняется в службе Azure с именем ContosoService03.</span><span class="sxs-lookup"><span data-stu-id="aee58-111">This command starts the virtual machine named VirtualMachine04 that runs in the Azure service named ContosoService03.</span></span>

### <span data-ttu-id="aee58-112">Пример 2: Запуск виртуальной машины с помощью объекта виртуальной машины</span><span class="sxs-lookup"><span data-stu-id="aee58-112">Example 2: Start a virtual machine by using a virtual machine object</span></span>
```
PS C:\> Get-AzureVM -ServiceName "ContosoService03" -Name "DatabaseServer" | Start-AzureVM
```

<span data-ttu-id="aee58-113">Эта команда извлекает объект виртуальной машины для виртуальной машины с именем DatabaseServer, а затем запросы на ее запуск.</span><span class="sxs-lookup"><span data-stu-id="aee58-113">This command retrieves the virtual machine object for the virtual machine whose name is DatabaseServer, and then requests to start it.</span></span>

## <span data-ttu-id="aee58-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="aee58-114">PARAMETERS</span></span>

### <span data-ttu-id="aee58-115">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="aee58-115">-InformationAction</span></span>
<span data-ttu-id="aee58-116">Указывает, как этот командлет отвечает на информационное событие.</span><span class="sxs-lookup"><span data-stu-id="aee58-116">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="aee58-117">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="aee58-117">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="aee58-118">Продолжал</span><span class="sxs-lookup"><span data-stu-id="aee58-118">Continue</span></span>
- <span data-ttu-id="aee58-119">Игнорируйте</span><span class="sxs-lookup"><span data-stu-id="aee58-119">Ignore</span></span>
- <span data-ttu-id="aee58-120">INQUIRE</span><span class="sxs-lookup"><span data-stu-id="aee58-120">Inquire</span></span>
- <span data-ttu-id="aee58-121">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="aee58-121">SilentlyContinue</span></span>
- <span data-ttu-id="aee58-122">Остановить</span><span class="sxs-lookup"><span data-stu-id="aee58-122">Stop</span></span>
- <span data-ttu-id="aee58-123">Рвать</span><span class="sxs-lookup"><span data-stu-id="aee58-123">Suspend</span></span>

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aee58-124">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="aee58-124">-InformationVariable</span></span>
<span data-ttu-id="aee58-125">Указывает переменную данных.</span><span class="sxs-lookup"><span data-stu-id="aee58-125">Specifies an information variable.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aee58-126">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="aee58-126">-Name</span></span>
<span data-ttu-id="aee58-127">Указывает имя виртуальной машины, которую нужно запустить.</span><span class="sxs-lookup"><span data-stu-id="aee58-127">Specifies the name of the virtual machine to start.</span></span>

```yaml
Type: String[]
Parameter Sets: ByName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aee58-128">-Profile</span><span class="sxs-lookup"><span data-stu-id="aee58-128">-Profile</span></span>
<span data-ttu-id="aee58-129">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="aee58-129">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="aee58-130">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="aee58-130">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="aee58-131">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="aee58-131">-ServiceName</span></span>
<span data-ttu-id="aee58-132">Указывает имя службы Azure, которая содержит виртуальную машину для запуска.</span><span class="sxs-lookup"><span data-stu-id="aee58-132">Specifies the name of the Azure service that contains the virtual machine to start.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aee58-133">-VM</span><span class="sxs-lookup"><span data-stu-id="aee58-133">-VM</span></span>
<span data-ttu-id="aee58-134">Указывает объект виртуальной машины, который определяет виртуальную машину для запуска.</span><span class="sxs-lookup"><span data-stu-id="aee58-134">Specifies a virtual machine object that identifies the virtual machine to start.</span></span>

```yaml
Type: IPersistentVM[]
Parameter Sets: Input
Aliases: InputObject

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aee58-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aee58-135">CommonParameters</span></span>
<span data-ttu-id="aee58-136">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="aee58-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aee58-137">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="aee58-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aee58-138">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="aee58-138">INPUTS</span></span>

## <span data-ttu-id="aee58-139">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="aee58-139">OUTPUTS</span></span>

## <span data-ttu-id="aee58-140">Пуск</span><span class="sxs-lookup"><span data-stu-id="aee58-140">NOTES</span></span>

## <span data-ttu-id="aee58-141">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="aee58-141">RELATED LINKS</span></span>

[<span data-ttu-id="aee58-142">Get-AzureVM</span><span class="sxs-lookup"><span data-stu-id="aee58-142">Get-AzureVM</span></span>](./Get-AzureVM.md)

[<span data-ttu-id="aee58-143">Remove-AzureVM</span><span class="sxs-lookup"><span data-stu-id="aee58-143">Remove-AzureVM</span></span>](./Remove-AzureVM.md)

[<span data-ttu-id="aee58-144">Restarts-AzureVM</span><span class="sxs-lookup"><span data-stu-id="aee58-144">Restart-AzureVM</span></span>](./Restart-AzureVM.md)

[<span data-ttu-id="aee58-145">Stop-AzureVM</span><span class="sxs-lookup"><span data-stu-id="aee58-145">Stop-AzureVM</span></span>](./Stop-AzureVM.md)

[<span data-ttu-id="aee58-146">Update-AzureVM</span><span class="sxs-lookup"><span data-stu-id="aee58-146">Update-AzureVM</span></span>](./Update-AzureVM.md)


