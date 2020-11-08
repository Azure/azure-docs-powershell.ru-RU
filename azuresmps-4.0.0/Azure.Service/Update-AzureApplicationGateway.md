---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: C7F08804-E177-4BC5-8F0E-DEC1B467C4BB
online version: ''
schema: 2.0.0
ms.openlocfilehash: 20cb37fbba8fd3789c0932f9ff1e9352334662e9
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94075844"
---
# <span data-ttu-id="cc6b2-101">Update-AzureApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="cc6b2-101">Update-AzureApplicationGateway</span></span>

## <span data-ttu-id="cc6b2-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="cc6b2-102">SYNOPSIS</span></span>
<span data-ttu-id="cc6b2-103">Обновляет шлюз приложения.</span><span class="sxs-lookup"><span data-stu-id="cc6b2-103">Updates an application gateway.</span></span>

## <span data-ttu-id="cc6b2-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="cc6b2-104">SYNTAX</span></span>

```
Update-AzureApplicationGateway -Name <String> [-VnetName <String>]
 [-Subnets <System.Collections.Generic.List`1[System.String]>] [-InstanceCount <UInt32>]
 [-GatewaySize <String>] [-Description <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="cc6b2-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="cc6b2-105">DESCRIPTION</span></span>
<span data-ttu-id="cc6b2-106">Командлет **Update-AzureApplicationGateway** обновляет существующий шлюз приложений.</span><span class="sxs-lookup"><span data-stu-id="cc6b2-106">The **Update-AzureApplicationGateway** cmdlet updates an existing application gateway.</span></span>

## <span data-ttu-id="cc6b2-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="cc6b2-107">EXAMPLES</span></span>

### <span data-ttu-id="cc6b2-108">Пример 1: изменение шлюза приложений с использованием его имени</span><span class="sxs-lookup"><span data-stu-id="cc6b2-108">Example 1: Modify an application gateway by using its name</span></span>
```
PS C:\> Stop-AzureApplicationGateway -Name "ApplicationGateway06"
PS C:\> Update-AzureApplicationGateway -Name "ApplicationGateway06" -VnetName "VirutalNetwork18" -Subnets @("Subnet05", "Subnet06")
```

<span data-ttu-id="cc6b2-109">Первая команда останавливает шлюз приложений с именем ApplicationGateway06.</span><span class="sxs-lookup"><span data-stu-id="cc6b2-109">The first command stops the application gateway named ApplicationGateway06.</span></span>
<span data-ttu-id="cc6b2-110">Прежде чем можно будет изменить виртуальную сеть или подсеть, необходимо остановить шлюз приложения.</span><span class="sxs-lookup"><span data-stu-id="cc6b2-110">An application gateway must be stopped before you can modify the virtual network or subnets.</span></span>

<span data-ttu-id="cc6b2-111">Вторая команда изменяет виртуальную подсеть и подсети для шлюза приложения с именем ApplicationGateway06.</span><span class="sxs-lookup"><span data-stu-id="cc6b2-111">The second command modifies the virtual subnet and subnets for the application gateway named ApplicationGateway06.</span></span>

### <span data-ttu-id="cc6b2-112">Пример 2: изменение дополнительных свойств шлюза приложения</span><span class="sxs-lookup"><span data-stu-id="cc6b2-112">Example 2: Modify additional properties of an application gateway</span></span>
```
PS C:\> Update-AzureApplicationGateway -Name "ApplicationGateway06" -InstanceCount 2 -GatewaySize "Large" -Description "Updated application gateway"
```

<span data-ttu-id="cc6b2-113">Эта команда изменяет количество экземпляров, размер шлюза и описание для шлюза приложения с именем ApplicationGateway06.</span><span class="sxs-lookup"><span data-stu-id="cc6b2-113">This command modifies the instance count, gateway size, and description for the application gateway named ApplicationGateway06.</span></span>
<span data-ttu-id="cc6b2-114">Эта команда не изменяет виртуальную сеть или подсети для шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="cc6b2-114">This command does not modify the virtual network or subnets for the application gateway.</span></span>
<span data-ttu-id="cc6b2-115">Таким образом, перед выполнением этой команды вам не нужно останавливать шлюз приложений.</span><span class="sxs-lookup"><span data-stu-id="cc6b2-115">Therefore, you do not have to stop the application gateway before you run this command.</span></span>

### <span data-ttu-id="cc6b2-116">Пример 3: изменение шлюза приложений с помощью конвейера</span><span class="sxs-lookup"><span data-stu-id="cc6b2-116">Example 3: Modify an application gateway by using the pipeline</span></span>
```
PS C:\> $ApplicationGateway = Get-AzureApplicationGateway -Name "ApplicationGateway06"
PS C:\> $ApplicationGateway.GatewaySize = "Medium"
PS C:\> $ApplicationGateway | Update-AzureApplicationGateway
```

<span data-ttu-id="cc6b2-117">Первая команда получает шлюз приложения с именем ApplicationGateway06 с помощью командлета **Get-AzureApplicationGateway** .</span><span class="sxs-lookup"><span data-stu-id="cc6b2-117">The first command gets the application gateway named ApplicationGateway06 by using the **Get-AzureApplicationGateway** cmdlet.</span></span>
<span data-ttu-id="cc6b2-118">Команда сохраняет его в переменной $ApplicationGateway.</span><span class="sxs-lookup"><span data-stu-id="cc6b2-118">The command stores it in the $ApplicationGateway variable.</span></span>

<span data-ttu-id="cc6b2-119">Вторая команда присваивает свойству **GatewaySize** значение Medium.</span><span class="sxs-lookup"><span data-stu-id="cc6b2-119">The second command assigns the **GatewaySize** property the value Medium.</span></span>

<span data-ttu-id="cc6b2-120">Последняя команда передает обновленный $ApplicationGateway текущему командлету.</span><span class="sxs-lookup"><span data-stu-id="cc6b2-120">The final command passes the updated $ApplicationGateway to the current cmdlet.</span></span>

## <span data-ttu-id="cc6b2-121">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="cc6b2-121">PARAMETERS</span></span>

### <span data-ttu-id="cc6b2-122">-Описание</span><span class="sxs-lookup"><span data-stu-id="cc6b2-122">-Description</span></span>
<span data-ttu-id="cc6b2-123">Указывает описание, назначаемое этим командлетом шлюзу приложений.</span><span class="sxs-lookup"><span data-stu-id="cc6b2-123">Specifies a description that this cmdlet assigns to the application gateway.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cc6b2-124">-GatewaySize</span><span class="sxs-lookup"><span data-stu-id="cc6b2-124">-GatewaySize</span></span>
<span data-ttu-id="cc6b2-125">Указывает размер, назначаемый этим командлетом шлюзу приложений.</span><span class="sxs-lookup"><span data-stu-id="cc6b2-125">Specifies the size that this cmdlet assigns to the application gateway.</span></span>
<span data-ttu-id="cc6b2-126">Допустимые значения:</span><span class="sxs-lookup"><span data-stu-id="cc6b2-126">Valid values are:</span></span>

- <span data-ttu-id="cc6b2-127">Малого</span><span class="sxs-lookup"><span data-stu-id="cc6b2-127">Small</span></span>
- <span data-ttu-id="cc6b2-128">Канал</span><span class="sxs-lookup"><span data-stu-id="cc6b2-128">Medium</span></span>
- <span data-ttu-id="cc6b2-129">Достаточ</span><span class="sxs-lookup"><span data-stu-id="cc6b2-129">Large</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cc6b2-130">-InstanceCount</span><span class="sxs-lookup"><span data-stu-id="cc6b2-130">-InstanceCount</span></span>
<span data-ttu-id="cc6b2-131">Указывает количество экземпляров, назначаемых этим командлетом шлюзу приложений.</span><span class="sxs-lookup"><span data-stu-id="cc6b2-131">Specifies the number of instances that this cmdlet assigns to the application gateway.</span></span>

```yaml
Type: UInt32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cc6b2-132">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="cc6b2-132">-Name</span></span>
<span data-ttu-id="cc6b2-133">Указывает имя шлюза приложений, который обновляется этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="cc6b2-133">Specifies the name of the application gateway that this cmdlet updates.</span></span>

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

### <span data-ttu-id="cc6b2-134">-Profile</span><span class="sxs-lookup"><span data-stu-id="cc6b2-134">-Profile</span></span>
<span data-ttu-id="cc6b2-135">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="cc6b2-135">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="cc6b2-136">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="cc6b2-136">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="cc6b2-137">-Подсети</span><span class="sxs-lookup"><span data-stu-id="cc6b2-137">-Subnets</span></span>
<span data-ttu-id="cc6b2-138">Указывает массив подсетей, в котором этот командлет развертывает шлюз приложения.</span><span class="sxs-lookup"><span data-stu-id="cc6b2-138">Specifies an array of subnets in which this cmdlet deploys the application gateway.</span></span>

<span data-ttu-id="cc6b2-139">Вы не можете обновлять подсети, пока запущен шлюз приложений.</span><span class="sxs-lookup"><span data-stu-id="cc6b2-139">You cannot update subnets while the application gateway is running.</span></span>
<span data-ttu-id="cc6b2-140">Чтобы остановить шлюз приложения, используйте командлет Stop-AzureApplicationGateway.</span><span class="sxs-lookup"><span data-stu-id="cc6b2-140">To stop the application gateway, use the Stop-AzureApplicationGateway cmdlet.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cc6b2-141">-VnetName</span><span class="sxs-lookup"><span data-stu-id="cc6b2-141">-VnetName</span></span>
<span data-ttu-id="cc6b2-142">Указывает виртуальную сеть, в которой этот командлет развертывает шлюз приложения.</span><span class="sxs-lookup"><span data-stu-id="cc6b2-142">Specifies the virtual network in which this cmdlet deploys the application gateway.</span></span>

<span data-ttu-id="cc6b2-143">Вы не можете обновить виртуальную сеть, пока запущен шлюз приложений.</span><span class="sxs-lookup"><span data-stu-id="cc6b2-143">You cannot update a virtual network while the application gateway is running.</span></span>
<span data-ttu-id="cc6b2-144">Чтобы остановить шлюз приложения, используйте **Stop-AzureApplicationGateway**.</span><span class="sxs-lookup"><span data-stu-id="cc6b2-144">To stop the application gateway, use **Stop-AzureApplicationGateway**.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cc6b2-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cc6b2-145">CommonParameters</span></span>
<span data-ttu-id="cc6b2-146">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="cc6b2-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cc6b2-147">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cc6b2-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cc6b2-148">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="cc6b2-148">INPUTS</span></span>

### <span data-ttu-id="cc6b2-149">System. String</span><span class="sxs-lookup"><span data-stu-id="cc6b2-149">System.String</span></span>

## <span data-ttu-id="cc6b2-150">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="cc6b2-150">OUTPUTS</span></span>

### <span data-ttu-id="cc6b2-151">Microsoft. WindowsAzure. Management. ApplicationGateway. Models. ApplicationGatewayOperationResponse</span><span class="sxs-lookup"><span data-stu-id="cc6b2-151">Microsoft.WindowsAzure.Management.ApplicationGateway.Models.ApplicationGatewayOperationResponse</span></span>

## <span data-ttu-id="cc6b2-152">Пуск</span><span class="sxs-lookup"><span data-stu-id="cc6b2-152">NOTES</span></span>

## <span data-ttu-id="cc6b2-153">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="cc6b2-153">RELATED LINKS</span></span>

[<span data-ttu-id="cc6b2-154">Get-AzureApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="cc6b2-154">Get-AzureApplicationGateway</span></span>](./Get-AzureApplicationGateway.md)

[<span data-ttu-id="cc6b2-155">New-AzureApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="cc6b2-155">New-AzureApplicationGateway</span></span>](./New-AzureApplicationGateway.md)

[<span data-ttu-id="cc6b2-156">Remove-AzureApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="cc6b2-156">Remove-AzureApplicationGateway</span></span>](./Remove-AzureApplicationGateway.md)

[<span data-ttu-id="cc6b2-157">Start-AzureApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="cc6b2-157">Start-AzureApplicationGateway</span></span>](./Start-AzureApplicationGateway.md)

[<span data-ttu-id="cc6b2-158">Остановить-AzureApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="cc6b2-158">Stop-AzureApplicationGateway</span></span>](./Stop-AzureApplicationGateway.md)
