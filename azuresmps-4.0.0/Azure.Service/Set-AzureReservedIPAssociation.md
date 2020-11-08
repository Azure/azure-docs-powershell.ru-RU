---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 3249E908-B1D9-4707-844D-168274F1A466
online version: ''
schema: 2.0.0
ms.openlocfilehash: ae16609adf70b2e5a0edcd05c36b30860a3920cf
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94075825"
---
# <span data-ttu-id="800a0-101">Set-AzureReservedIPAssociation</span><span class="sxs-lookup"><span data-stu-id="800a0-101">Set-AzureReservedIPAssociation</span></span>

## <span data-ttu-id="800a0-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="800a0-102">SYNOPSIS</span></span>
<span data-ttu-id="800a0-103">Связывает зарезервированный IP-адрес с существующей виртуальной машиной или облачной службой.</span><span class="sxs-lookup"><span data-stu-id="800a0-103">Associates a reserved IP address with an existing virtual machine or cloud service.</span></span>

## <span data-ttu-id="800a0-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="800a0-104">SYNTAX</span></span>

```
Set-AzureReservedIPAssociation [-ReservedIPName] <String> [-ServiceName] <String> [[-VirtualIPName] <String>]
 [[-Slot] <String>] [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="800a0-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="800a0-105">DESCRIPTION</span></span>
<span data-ttu-id="800a0-106">Командлет **Set-AzureReservedIPAssociation** связывает зарезервированный IP-адрес с ВИРТУАЛЬНЫМ IP-адресом (VIP) запущенной виртуальной машины или облачной службы.</span><span class="sxs-lookup"><span data-stu-id="800a0-106">The **Set-AzureReservedIPAssociation** cmdlet associates a reserved IP address with the Virtual IP address (VIP) of a running virtual machine or cloud service.</span></span>
<span data-ttu-id="800a0-107">Зарезервированный IP-адрес нельзя использовать во время вызова этого командлета и должен находиться в том же регионе, что и виртуальная машина или облачная служба.</span><span class="sxs-lookup"><span data-stu-id="800a0-107">The reserved IP address must not be in use at the time of invocation of this cmdlet, and must be in the same region as the virtual machine or cloud service.</span></span>

<span data-ttu-id="800a0-108">Выполнение операции займет около 30 секунд, после чего виртуальная машина или служба будет доступна с помощью зарезервированного IP-адреса.</span><span class="sxs-lookup"><span data-stu-id="800a0-108">The operation takes about 30 seconds to complete, after which the virtual machine or service is accessible using the reserved IP address.</span></span>

## <span data-ttu-id="800a0-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="800a0-109">EXAMPLES</span></span>

### <span data-ttu-id="800a0-110">Пример 1: Настройка зарезервированной IP-связи</span><span class="sxs-lookup"><span data-stu-id="800a0-110">Example 1: Set a reserved IP association</span></span>
```
PS C:\> Set-AzureReservedIPAssociation -ReservedIPName "ResIp14" -ServiceName "PipTestWestEurope"
```

<span data-ttu-id="800a0-111">Эта команда назначает зарезервированный IP-адрес с именем ResIp14 для службы PipTestWestEurope.</span><span class="sxs-lookup"><span data-stu-id="800a0-111">This command assigns the reserved IP address named ResIp14 to the service PipTestWestEurope.</span></span>
<span data-ttu-id="800a0-112">ResIp14 — это зарезервированный IP-адрес в регионе "Западная Европа".</span><span class="sxs-lookup"><span data-stu-id="800a0-112">ResIp14 is a reserved IP in the West Europe region.</span></span>

## <span data-ttu-id="800a0-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="800a0-113">PARAMETERS</span></span>

### <span data-ttu-id="800a0-114">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="800a0-114">-InformationAction</span></span>
<span data-ttu-id="800a0-115">Указывает, как этот командлет отвечает на информационное событие.</span><span class="sxs-lookup"><span data-stu-id="800a0-115">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="800a0-116">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="800a0-116">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="800a0-117">Продолжал</span><span class="sxs-lookup"><span data-stu-id="800a0-117">Continue</span></span>
- <span data-ttu-id="800a0-118">Игнорируйте</span><span class="sxs-lookup"><span data-stu-id="800a0-118">Ignore</span></span>
- <span data-ttu-id="800a0-119">INQUIRE</span><span class="sxs-lookup"><span data-stu-id="800a0-119">Inquire</span></span>
- <span data-ttu-id="800a0-120">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="800a0-120">SilentlyContinue</span></span>
- <span data-ttu-id="800a0-121">Остановить</span><span class="sxs-lookup"><span data-stu-id="800a0-121">Stop</span></span>
- <span data-ttu-id="800a0-122">Рвать</span><span class="sxs-lookup"><span data-stu-id="800a0-122">Suspend</span></span>

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

### <span data-ttu-id="800a0-123">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="800a0-123">-InformationVariable</span></span>
<span data-ttu-id="800a0-124">Указывает переменную данных.</span><span class="sxs-lookup"><span data-stu-id="800a0-124">Specifies an information variable.</span></span>

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

### <span data-ttu-id="800a0-125">-Profile</span><span class="sxs-lookup"><span data-stu-id="800a0-125">-Profile</span></span>
<span data-ttu-id="800a0-126">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="800a0-126">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="800a0-127">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="800a0-127">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="800a0-128">-ReservedIPName</span><span class="sxs-lookup"><span data-stu-id="800a0-128">-ReservedIPName</span></span>
<span data-ttu-id="800a0-129">Задает имя зарезервированного IP-адреса, связанного с виртуальной машиной или службой.</span><span class="sxs-lookup"><span data-stu-id="800a0-129">Specifies the name of the reserved IP address to associate with a virtual machine or service.</span></span>

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

### <span data-ttu-id="800a0-130">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="800a0-130">-ServiceName</span></span>
<span data-ttu-id="800a0-131">Указывает имя службы, для которой установлено развертывание, с которым нужно связать зарезервированный IP-адрес.</span><span class="sxs-lookup"><span data-stu-id="800a0-131">Specifies the name of the service that has the deployment with which to associate the reserved IP address.</span></span>

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

### <span data-ttu-id="800a0-132">-Slot</span><span class="sxs-lookup"><span data-stu-id="800a0-132">-Slot</span></span>
<span data-ttu-id="800a0-133">Указывает слот развертывания.</span><span class="sxs-lookup"><span data-stu-id="800a0-133">Specifies the deployment slot.</span></span>
<span data-ttu-id="800a0-134">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="800a0-134">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="800a0-135">Промежуточного хранения</span><span class="sxs-lookup"><span data-stu-id="800a0-135">Staging</span></span>
- <span data-ttu-id="800a0-136">Спецификации</span><span class="sxs-lookup"><span data-stu-id="800a0-136">Production</span></span>

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

### <span data-ttu-id="800a0-137">-VirtualIPName</span><span class="sxs-lookup"><span data-stu-id="800a0-137">-VirtualIPName</span></span>
<span data-ttu-id="800a0-138">Указывает имя существующего виртуального IP-адреса, связанного с зарезервированным IP.</span><span class="sxs-lookup"><span data-stu-id="800a0-138">Specifies the name of an existing VIP to associate with a reserved IP.</span></span>
<span data-ttu-id="800a0-139">Чтобы добавить VIP в облачную службу, просмотрите Add-AzureVirtualIP.</span><span class="sxs-lookup"><span data-stu-id="800a0-139">See Add-AzureVirtualIP to add VIPs to your cloud service.</span></span>

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

### <span data-ttu-id="800a0-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="800a0-140">CommonParameters</span></span>
<span data-ttu-id="800a0-141">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="800a0-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="800a0-142">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="800a0-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="800a0-143">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="800a0-143">INPUTS</span></span>

## <span data-ttu-id="800a0-144">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="800a0-144">OUTPUTS</span></span>

### <span data-ttu-id="800a0-145">Microsoft. WindowsAzure. Commands. Utilities. Common. ManagementOperationContext</span><span class="sxs-lookup"><span data-stu-id="800a0-145">Microsoft.WindowsAzure.Commands.Utilities.Common.ManagementOperationContext</span></span>

## <span data-ttu-id="800a0-146">Пуск</span><span class="sxs-lookup"><span data-stu-id="800a0-146">NOTES</span></span>

## <span data-ttu-id="800a0-147">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="800a0-147">RELATED LINKS</span></span>

[<span data-ttu-id="800a0-148">Remove-AzureReservedIPAssociation</span><span class="sxs-lookup"><span data-stu-id="800a0-148">Remove-AzureReservedIPAssociation</span></span>](./Remove-AzureReservedIPAssociation.md)


