---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 437889D1-F24F-4BBE-8C56-7C3E48CEA517
online version: ''
schema: 2.0.0
ms.openlocfilehash: 86dd38ce7fa55507be3362c1494b88df491a1067
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94075791"
---
# <span data-ttu-id="23fb4-101">Set-AzureVMSize</span><span class="sxs-lookup"><span data-stu-id="23fb4-101">Set-AzureVMSize</span></span>

## <span data-ttu-id="23fb4-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="23fb4-102">SYNOPSIS</span></span>
<span data-ttu-id="23fb4-103">Задает размер виртуальной машины Azure.</span><span class="sxs-lookup"><span data-stu-id="23fb4-103">Sets the size of an Azure virtual machine.</span></span>

## <span data-ttu-id="23fb4-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="23fb4-104">SYNTAX</span></span>

```
Set-AzureVMSize [-InstanceSize] <String> -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="23fb4-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="23fb4-105">DESCRIPTION</span></span>
<span data-ttu-id="23fb4-106">Командлет **Set-AzureVMSize** обновляет размер виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="23fb4-106">The **Set-AzureVMSize** cmdlet updates the size of a virtual machine.</span></span>
<span data-ttu-id="23fb4-107">У него есть два параметра: *InstanceSize* , который является новым размером виртуальной машины и *ВМ* , которая является объектом виртуальной машины, извлеченным с помощью командлета **Get-AzureVM** .</span><span class="sxs-lookup"><span data-stu-id="23fb4-107">It has two parameters: *InstanceSize* , which is the new size of the virtual machine, and *VM* , which is a virtual machine object retrieved by using the **Get-AzureVM** cmdlet.</span></span>
<span data-ttu-id="23fb4-108">Результат **Set-AzureVMSize** можно передать командлету **Update-AzureVM** или сохранить его в переменной для последующего использования.</span><span class="sxs-lookup"><span data-stu-id="23fb4-108">The result of **Set-AzureVMSize** can be piped to the **Update-AzureVM** cmdlet or stored in a variable for later use.</span></span>
<span data-ttu-id="23fb4-109">Фактическое изменение не выполняется до тех пор, пока не будет выполнена **Update-AzureVM** .</span><span class="sxs-lookup"><span data-stu-id="23fb4-109">No actual change is made until **Update-AzureVM** is executed.</span></span>

<span data-ttu-id="23fb4-110">Примечание. для этого командлета потребуется повторное наполнение виртуальной машины, и может быть получен новый IP-адрес.</span><span class="sxs-lookup"><span data-stu-id="23fb4-110">Note: This cmdlet will require the virtual machine to be re-provisioned and it might get a new IP address.</span></span>

## <span data-ttu-id="23fb4-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="23fb4-111">EXAMPLES</span></span>

### <span data-ttu-id="23fb4-112">Пример 1: Установка размера виртуальной машины</span><span class="sxs-lookup"><span data-stu-id="23fb4-112">Example 1: Set the size of a virtual machine</span></span>
```
PS C:\> Get-AzureVM -ServiceName "MySvc1" -Name "MyVM3" | Set-AzureVMSize "Small" | Update-AzureVM
```

<span data-ttu-id="23fb4-113">Эта команда обновляет виртуальную машину на размер "Малый".</span><span class="sxs-lookup"><span data-stu-id="23fb4-113">This command updates a virtual machine to size "Small".</span></span>

## <span data-ttu-id="23fb4-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="23fb4-114">PARAMETERS</span></span>

### <span data-ttu-id="23fb4-115">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="23fb4-115">-InformationAction</span></span>
<span data-ttu-id="23fb4-116">Указывает, как этот командлет отвечает на информационное событие.</span><span class="sxs-lookup"><span data-stu-id="23fb4-116">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="23fb4-117">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="23fb4-117">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="23fb4-118">Продолжал</span><span class="sxs-lookup"><span data-stu-id="23fb4-118">Continue</span></span>
- <span data-ttu-id="23fb4-119">Игнорируйте</span><span class="sxs-lookup"><span data-stu-id="23fb4-119">Ignore</span></span>
- <span data-ttu-id="23fb4-120">INQUIRE</span><span class="sxs-lookup"><span data-stu-id="23fb4-120">Inquire</span></span>
- <span data-ttu-id="23fb4-121">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="23fb4-121">SilentlyContinue</span></span>
- <span data-ttu-id="23fb4-122">Остановить</span><span class="sxs-lookup"><span data-stu-id="23fb4-122">Stop</span></span>
- <span data-ttu-id="23fb4-123">Рвать</span><span class="sxs-lookup"><span data-stu-id="23fb4-123">Suspend</span></span>

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

### <span data-ttu-id="23fb4-124">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="23fb4-124">-InformationVariable</span></span>
<span data-ttu-id="23fb4-125">Указывает переменную данных.</span><span class="sxs-lookup"><span data-stu-id="23fb4-125">Specifies an information variable.</span></span>

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

### <span data-ttu-id="23fb4-126">-InstanceSize</span><span class="sxs-lookup"><span data-stu-id="23fb4-126">-InstanceSize</span></span>
<span data-ttu-id="23fb4-127">Задает размер виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="23fb4-127">Specifies the size of the virtual machine.</span></span>

<span data-ttu-id="23fb4-128">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="23fb4-128">The acceptable values for this parameter are:</span></span>

<span data-ttu-id="23fb4-129">---Мелкий--, ExtraSmall--— для ExtraLarge--, A5 – 7 – A6</span><span class="sxs-lookup"><span data-stu-id="23fb4-129">--ExtraSmall --Small --Medium --Large --ExtraLarge --A5 --A6 --A7</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="23fb4-130">-Profile</span><span class="sxs-lookup"><span data-stu-id="23fb4-130">-Profile</span></span>
<span data-ttu-id="23fb4-131">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="23fb4-131">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="23fb4-132">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="23fb4-132">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="23fb4-133">-VM</span><span class="sxs-lookup"><span data-stu-id="23fb4-133">-VM</span></span>
<span data-ttu-id="23fb4-134">Указывает Сохраняемый объект виртуальной машины, размер которого задает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="23fb4-134">Specifies the persistent virtual machine object that this cmdlet sets the size of.</span></span>

```yaml
Type: IPersistentVM
Parameter Sets: (All)
Aliases: InputObject

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="23fb4-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="23fb4-135">CommonParameters</span></span>
<span data-ttu-id="23fb4-136">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="23fb4-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="23fb4-137">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="23fb4-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="23fb4-138">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="23fb4-138">INPUTS</span></span>

## <span data-ttu-id="23fb4-139">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="23fb4-139">OUTPUTS</span></span>

## <span data-ttu-id="23fb4-140">Пуск</span><span class="sxs-lookup"><span data-stu-id="23fb4-140">NOTES</span></span>

## <span data-ttu-id="23fb4-141">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="23fb4-141">RELATED LINKS</span></span>

[<span data-ttu-id="23fb4-142">Get-AzureVM</span><span class="sxs-lookup"><span data-stu-id="23fb4-142">Get-AzureVM</span></span>](./Get-AzureVM.md)

[<span data-ttu-id="23fb4-143">Update-AzureVM</span><span class="sxs-lookup"><span data-stu-id="23fb4-143">Update-AzureVM</span></span>](./Update-AzureVM.md)


