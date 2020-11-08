---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: A6964C80-1991-46FC-84C8-5B00616386BE
online version: ''
schema: 2.0.0
ms.openlocfilehash: 9e43f841fea77626c18edbda541fa011e95faceb
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94076136"
---
# <span data-ttu-id="fbdfa-101">Remove-AzureReservedIPAssociation</span><span class="sxs-lookup"><span data-stu-id="fbdfa-101">Remove-AzureReservedIPAssociation</span></span>

## <span data-ttu-id="fbdfa-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="fbdfa-102">SYNOPSIS</span></span>
<span data-ttu-id="fbdfa-103">Удаляет связь с зарезервированным IP-адресом в виртуальной машине или в облачной службе.</span><span class="sxs-lookup"><span data-stu-id="fbdfa-103">Removes the association from the reserved IP address to the VM or cloud service.</span></span>

## <span data-ttu-id="fbdfa-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="fbdfa-104">SYNTAX</span></span>

```
Remove-AzureReservedIPAssociation [-ReservedIPName] <String> [-ServiceName] <String>
 [[-VirtualIPName] <String>] [[-Slot] <String>] [-Force] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="fbdfa-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="fbdfa-105">DESCRIPTION</span></span>
<span data-ttu-id="fbdfa-106">Командлет **Remove-AzureReservedIPAssociation удаляет** зарезервированный IP-адрес из виртуальной машины (ВМ) или облачной службы.</span><span class="sxs-lookup"><span data-stu-id="fbdfa-106">The **Remove-AzureReservedIPAssociation** cmdlet disassociates a reserved IP address from a virtual machine (VM) or Cloud Service.</span></span>
<span data-ttu-id="fbdfa-107">По завершении операции зарезервированный IP-адрес свободен, а VM/VIP получает динамический публичный IP-адрес из описи Azure.</span><span class="sxs-lookup"><span data-stu-id="fbdfa-107">When the operation completes, the reserved IP address is free and the VM/VIP gets a dynamic public IP Address from the Azure Inventory.</span></span>

## <span data-ttu-id="fbdfa-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="fbdfa-108">EXAMPLES</span></span>

### <span data-ttu-id="fbdfa-109">Пример 1: удаление зарезервированной IP-связи</span><span class="sxs-lookup"><span data-stu-id="fbdfa-109">Example 1: Remove a reserved IP association</span></span>
```
PS C:\> Remove-AzureReservedIPAssociation -ReservedIPName "ResIp14" -ServiceName "PipTestWestEurope"
```

<span data-ttu-id="fbdfa-110">Эта команда разрывает зарезервированный IP-адрес с именем ResIp14 из службы с именем PipTestWestEurope.</span><span class="sxs-lookup"><span data-stu-id="fbdfa-110">This command disassociates the reserved IP address named ResIp14 from the service named PipTestWestEurope.</span></span>
<span data-ttu-id="fbdfa-111">PipTestWestEurope будет назначен новый динамический виртуальный IP-адрес.</span><span class="sxs-lookup"><span data-stu-id="fbdfa-111">PipTestWestEurope will be assigned a new dynamic VIP.</span></span>

## <span data-ttu-id="fbdfa-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="fbdfa-112">PARAMETERS</span></span>

### <span data-ttu-id="fbdfa-113">-Force</span><span class="sxs-lookup"><span data-stu-id="fbdfa-113">-Force</span></span>
<span data-ttu-id="fbdfa-114">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="fbdfa-114">Forces the command to run without asking for user confirmation.</span></span>

<span data-ttu-id="fbdfa-115">Этот флаг используется для обхода предупреждающих сообщений при удалении зарезервированной IP-связи.</span><span class="sxs-lookup"><span data-stu-id="fbdfa-115">Use this flag to bypass warning messages when removing the reserved IP association.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fbdfa-116">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="fbdfa-116">-InformationAction</span></span>
<span data-ttu-id="fbdfa-117">Указывает, как этот командлет отвечает на информационное событие.</span><span class="sxs-lookup"><span data-stu-id="fbdfa-117">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="fbdfa-118">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="fbdfa-118">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="fbdfa-119">Продолжал</span><span class="sxs-lookup"><span data-stu-id="fbdfa-119">Continue</span></span>
- <span data-ttu-id="fbdfa-120">Игнорируйте</span><span class="sxs-lookup"><span data-stu-id="fbdfa-120">Ignore</span></span>
- <span data-ttu-id="fbdfa-121">INQUIRE</span><span class="sxs-lookup"><span data-stu-id="fbdfa-121">Inquire</span></span>
- <span data-ttu-id="fbdfa-122">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="fbdfa-122">SilentlyContinue</span></span>
- <span data-ttu-id="fbdfa-123">Остановить</span><span class="sxs-lookup"><span data-stu-id="fbdfa-123">Stop</span></span>
- <span data-ttu-id="fbdfa-124">Рвать</span><span class="sxs-lookup"><span data-stu-id="fbdfa-124">Suspend</span></span>

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

### <span data-ttu-id="fbdfa-125">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="fbdfa-125">-InformationVariable</span></span>
<span data-ttu-id="fbdfa-126">Указывает переменную данных.</span><span class="sxs-lookup"><span data-stu-id="fbdfa-126">Specifies an information variable.</span></span>

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

### <span data-ttu-id="fbdfa-127">-Profile</span><span class="sxs-lookup"><span data-stu-id="fbdfa-127">-Profile</span></span>
<span data-ttu-id="fbdfa-128">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="fbdfa-128">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="fbdfa-129">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="fbdfa-129">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="fbdfa-130">-ReservedIPName</span><span class="sxs-lookup"><span data-stu-id="fbdfa-130">-ReservedIPName</span></span>
<span data-ttu-id="fbdfa-131">Задает имя зарезервированного IP-адреса.</span><span class="sxs-lookup"><span data-stu-id="fbdfa-131">Specifies the name of the reserved IP address.</span></span>

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

### <span data-ttu-id="fbdfa-132">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="fbdfa-132">-ServiceName</span></span>
<span data-ttu-id="fbdfa-133">Указывает имя службы.</span><span class="sxs-lookup"><span data-stu-id="fbdfa-133">Specifies the  name of the service.</span></span>

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

### <span data-ttu-id="fbdfa-134">-Slot</span><span class="sxs-lookup"><span data-stu-id="fbdfa-134">-Slot</span></span>
<span data-ttu-id="fbdfa-135">Указывает среду развертывания.</span><span class="sxs-lookup"><span data-stu-id="fbdfa-135">Specifies the deployment environment.</span></span>
<span data-ttu-id="fbdfa-136">Допустимые значения этого параметра: "производство", "промежуточный".</span><span class="sxs-lookup"><span data-stu-id="fbdfa-136">The acceptable values for this parameter are: Production, Staging.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fbdfa-137">-VirtualIPName</span><span class="sxs-lookup"><span data-stu-id="fbdfa-137">-VirtualIPName</span></span>
<span data-ttu-id="fbdfa-138">Задает виртуальный IP-адрес, с которого будет удалена связь со службой или виртуальной машиной.</span><span class="sxs-lookup"><span data-stu-id="fbdfa-138">Specifies a virtual IP address from which to remove the association with a service or VM.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fbdfa-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fbdfa-139">CommonParameters</span></span>
<span data-ttu-id="fbdfa-140">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="fbdfa-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fbdfa-141">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fbdfa-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fbdfa-142">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="fbdfa-142">INPUTS</span></span>

## <span data-ttu-id="fbdfa-143">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="fbdfa-143">OUTPUTS</span></span>

### <span data-ttu-id="fbdfa-144">Microsoft. WindowsAzure. Commands. Utilities. Common. ManagementOperationContext</span><span class="sxs-lookup"><span data-stu-id="fbdfa-144">Microsoft.WindowsAzure.Commands.Utilities.Common.ManagementOperationContext</span></span>

## <span data-ttu-id="fbdfa-145">Пуск</span><span class="sxs-lookup"><span data-stu-id="fbdfa-145">NOTES</span></span>

## <span data-ttu-id="fbdfa-146">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="fbdfa-146">RELATED LINKS</span></span>

[<span data-ttu-id="fbdfa-147">Set-AzureReservedIPAssociation</span><span class="sxs-lookup"><span data-stu-id="fbdfa-147">Set-AzureReservedIPAssociation</span></span>](./Set-AzureReservedIPAssociation.md)


