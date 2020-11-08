---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: E0590AD4-F67B-48EF-8657-8890A2204CB6
online version: ''
schema: 2.0.0
ms.openlocfilehash: 607cd288bcc9c86209a3ae0af569e964205f5cb4
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94076067"
---
# <span data-ttu-id="d032d-101">Set-AzureAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="d032d-101">Set-AzureAvailabilitySet</span></span>

## <span data-ttu-id="d032d-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="d032d-102">SYNOPSIS</span></span>
<span data-ttu-id="d032d-103">Задает имя группы доступности на виртуальной машине Azure.</span><span class="sxs-lookup"><span data-stu-id="d032d-103">Sets the name of the availability set on an Azure virtual machine.</span></span>

## <span data-ttu-id="d032d-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="d032d-104">SYNTAX</span></span>

```
Set-AzureAvailabilitySet [-AvailabilitySetName] <String> -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="d032d-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d032d-105">DESCRIPTION</span></span>
<span data-ttu-id="d032d-106">Командлет **Set-AzureAvailabilitySet** задает имя группы доступности на виртуальной машине Azure после развертывания.</span><span class="sxs-lookup"><span data-stu-id="d032d-106">The **Set-AzureAvailabilitySet** cmdlet sets the name of the availability set on an Azure virtual machine after deployment.</span></span>

## <span data-ttu-id="d032d-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="d032d-107">EXAMPLES</span></span>

### <span data-ttu-id="d032d-108">Пример 1: изменение имени группы доступности</span><span class="sxs-lookup"><span data-stu-id="d032d-108">Example 1: Modify the name of an availability set</span></span>
```
PS C:\> Get-AzureVM -ServiceName "ContosoService" -Name "VirtualMachine24" | Set-AzureAvailabilitySet -AvailabilitySetName "AvailabilitySet14" | Update-AzureVM
```

<span data-ttu-id="d032d-109">Первая команда получает виртуальную машину с именем VirtualMachine07 в службе с именем ContosoService с помощью командлета **Get-AzureVM** .</span><span class="sxs-lookup"><span data-stu-id="d032d-109">The first command gets the virtual machine named VirtualMachine07 in the service named ContosoService by using the **Get-AzureVM** cmdlet.</span></span>
<span data-ttu-id="d032d-110">Команда передает этот объект в текущий командлет с помощью оператора конвейера.</span><span class="sxs-lookup"><span data-stu-id="d032d-110">The command passes that object to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="d032d-111">Этот командлет изменяет имя группы доступности для этой виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="d032d-111">That cmdlet modifies the name of the availability set for that virtual machine.</span></span>
<span data-ttu-id="d032d-112">Эта команда обновляет виртуальную машину.</span><span class="sxs-lookup"><span data-stu-id="d032d-112">The command updates the virtual machine.</span></span>

## <span data-ttu-id="d032d-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="d032d-113">PARAMETERS</span></span>

### <span data-ttu-id="d032d-114">-AvailabilitySetName</span><span class="sxs-lookup"><span data-stu-id="d032d-114">-AvailabilitySetName</span></span>
<span data-ttu-id="d032d-115">Указывает имя группы доступности, в которую входит виртуальная машина.</span><span class="sxs-lookup"><span data-stu-id="d032d-115">Specifies the name of the availability set to which the virtual machine belongs.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d032d-116">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="d032d-116">-InformationAction</span></span>
<span data-ttu-id="d032d-117">Указывает, как этот командлет отвечает на информационное событие.</span><span class="sxs-lookup"><span data-stu-id="d032d-117">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="d032d-118">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="d032d-118">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="d032d-119">Продолжал</span><span class="sxs-lookup"><span data-stu-id="d032d-119">Continue</span></span>
- <span data-ttu-id="d032d-120">Игнорируйте</span><span class="sxs-lookup"><span data-stu-id="d032d-120">Ignore</span></span>
- <span data-ttu-id="d032d-121">INQUIRE</span><span class="sxs-lookup"><span data-stu-id="d032d-121">Inquire</span></span>
- <span data-ttu-id="d032d-122">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="d032d-122">SilentlyContinue</span></span>
- <span data-ttu-id="d032d-123">Остановить</span><span class="sxs-lookup"><span data-stu-id="d032d-123">Stop</span></span>
- <span data-ttu-id="d032d-124">Рвать</span><span class="sxs-lookup"><span data-stu-id="d032d-124">Suspend</span></span>

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

### <span data-ttu-id="d032d-125">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="d032d-125">-InformationVariable</span></span>
<span data-ttu-id="d032d-126">Указывает переменную данных.</span><span class="sxs-lookup"><span data-stu-id="d032d-126">Specifies an information variable.</span></span>

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

### <span data-ttu-id="d032d-127">-Profile</span><span class="sxs-lookup"><span data-stu-id="d032d-127">-Profile</span></span>
<span data-ttu-id="d032d-128">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="d032d-128">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="d032d-129">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="d032d-129">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="d032d-130">-VM</span><span class="sxs-lookup"><span data-stu-id="d032d-130">-VM</span></span>
<span data-ttu-id="d032d-131">Указывает конфигурацию виртуальной машины, которую изменяет этот командлет.</span><span class="sxs-lookup"><span data-stu-id="d032d-131">Specifies the virtual machine configuration that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="d032d-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d032d-132">CommonParameters</span></span>
<span data-ttu-id="d032d-133">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="d032d-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d032d-134">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d032d-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d032d-135">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="d032d-135">INPUTS</span></span>

## <span data-ttu-id="d032d-136">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="d032d-136">OUTPUTS</span></span>

## <span data-ttu-id="d032d-137">Пуск</span><span class="sxs-lookup"><span data-stu-id="d032d-137">NOTES</span></span>

## <span data-ttu-id="d032d-138">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d032d-138">RELATED LINKS</span></span>

[<span data-ttu-id="d032d-139">Get-AzureVM</span><span class="sxs-lookup"><span data-stu-id="d032d-139">Get-AzureVM</span></span>](./Get-AzureVM.md)

[<span data-ttu-id="d032d-140">Remove-AzureAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="d032d-140">Remove-AzureAvailabilitySet</span></span>](./Remove-AzureAvailabilitySet.md)


