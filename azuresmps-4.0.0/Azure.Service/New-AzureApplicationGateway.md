---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: BED3D3FE-D1E8-4857-A675-7B2670A129B2
online version: ''
schema: 2.0.0
ms.openlocfilehash: 039afbea4d4eb6736cf3b0faebf189edef2d9c26
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94076226"
---
# <span data-ttu-id="73c2c-101">New-AzureApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="73c2c-101">New-AzureApplicationGateway</span></span>

## <span data-ttu-id="73c2c-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="73c2c-102">SYNOPSIS</span></span>
<span data-ttu-id="73c2c-103">Создание шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="73c2c-103">Creates an application gateway.</span></span>

## <span data-ttu-id="73c2c-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="73c2c-104">SYNTAX</span></span>

```
New-AzureApplicationGateway -Name <String> -VnetName <String>
 -Subnets <System.Collections.Generic.List`1[System.String]> [-InstanceCount <UInt32>] [-GatewaySize <String>]
 [-Description <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="73c2c-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="73c2c-105">DESCRIPTION</span></span>
<span data-ttu-id="73c2c-106">Командлет **New-AzureApplicationGateway** создает шлюз приложений.</span><span class="sxs-lookup"><span data-stu-id="73c2c-106">The **New-AzureApplicationGateway** cmdlet creates an application gateway.</span></span>

## <span data-ttu-id="73c2c-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="73c2c-107">EXAMPLES</span></span>

### <span data-ttu-id="73c2c-108">Пример 1: Создание шлюза приложений</span><span class="sxs-lookup"><span data-stu-id="73c2c-108">Example 1: Create an application gateway</span></span>
```
PS C:\> New-AzureApplicationGateway -Name "ApplicationGateway06" -VnetName "VirutalNetwork17" -Subnets @("Subnet01", "Subnet02", "Subnet03")
```

<span data-ttu-id="73c2c-109">Эта команда создает шлюз приложений с именем ApplicationGateway06.</span><span class="sxs-lookup"><span data-stu-id="73c2c-109">This command creates an application gateway named ApplicationGateway06.</span></span>
<span data-ttu-id="73c2c-110">Команда развертывает шлюз в VirtualNetwork17 и в заданной подсети.</span><span class="sxs-lookup"><span data-stu-id="73c2c-110">The command deploys the gateway in VirtualNetwork17 and in the specified subnets.</span></span>

## <span data-ttu-id="73c2c-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="73c2c-111">PARAMETERS</span></span>

### <span data-ttu-id="73c2c-112">-Описание</span><span class="sxs-lookup"><span data-stu-id="73c2c-112">-Description</span></span>
<span data-ttu-id="73c2c-113">Указывает описание, назначаемое этим командлетом шлюзу приложений.</span><span class="sxs-lookup"><span data-stu-id="73c2c-113">Specifies a description that this cmdlet assigns to the application gateway.</span></span>

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

### <span data-ttu-id="73c2c-114">-GatewaySize</span><span class="sxs-lookup"><span data-stu-id="73c2c-114">-GatewaySize</span></span>
<span data-ttu-id="73c2c-115">Указывает размер, назначаемый этим командлетом шлюзу приложений.</span><span class="sxs-lookup"><span data-stu-id="73c2c-115">Specifies the size that this cmdlet assigns to the application gateway.</span></span>
<span data-ttu-id="73c2c-116">Допустимые значения:</span><span class="sxs-lookup"><span data-stu-id="73c2c-116">Valid values are:</span></span>

- <span data-ttu-id="73c2c-117">Малого</span><span class="sxs-lookup"><span data-stu-id="73c2c-117">Small</span></span>
- <span data-ttu-id="73c2c-118">Канал</span><span class="sxs-lookup"><span data-stu-id="73c2c-118">Medium</span></span>
- <span data-ttu-id="73c2c-119">Достаточ</span><span class="sxs-lookup"><span data-stu-id="73c2c-119">Large</span></span>

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

### <span data-ttu-id="73c2c-120">-InstanceCount</span><span class="sxs-lookup"><span data-stu-id="73c2c-120">-InstanceCount</span></span>
<span data-ttu-id="73c2c-121">Указывает количество экземпляров, назначаемых этим командлетом шлюзу приложений.</span><span class="sxs-lookup"><span data-stu-id="73c2c-121">Specifies the number of instances that this cmdlet assigns to the application gateway.</span></span>

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

### <span data-ttu-id="73c2c-122">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="73c2c-122">-Name</span></span>
<span data-ttu-id="73c2c-123">Указывает имя нового шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="73c2c-123">Specifies a name for the new application gateway.</span></span>

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

### <span data-ttu-id="73c2c-124">-Profile</span><span class="sxs-lookup"><span data-stu-id="73c2c-124">-Profile</span></span>
<span data-ttu-id="73c2c-125">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="73c2c-125">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="73c2c-126">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="73c2c-126">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="73c2c-127">-Подсети</span><span class="sxs-lookup"><span data-stu-id="73c2c-127">-Subnets</span></span>
<span data-ttu-id="73c2c-128">Указывает массив подсетей, в котором этот командлет развертывает шлюз приложения.</span><span class="sxs-lookup"><span data-stu-id="73c2c-128">Specifies an array of subnets in which this cmdlet deploys the application gateway.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="73c2c-129">-VnetName</span><span class="sxs-lookup"><span data-stu-id="73c2c-129">-VnetName</span></span>
<span data-ttu-id="73c2c-130">Указывает виртуальную сеть, в которой этот командлет развертывает шлюз приложения.</span><span class="sxs-lookup"><span data-stu-id="73c2c-130">Specifies the virtual network in which this cmdlet deploys the application gateway.</span></span>

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

### <span data-ttu-id="73c2c-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="73c2c-131">CommonParameters</span></span>
<span data-ttu-id="73c2c-132">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="73c2c-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="73c2c-133">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="73c2c-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="73c2c-134">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="73c2c-134">INPUTS</span></span>

### <span data-ttu-id="73c2c-135">System. String</span><span class="sxs-lookup"><span data-stu-id="73c2c-135">System.String</span></span>

## <span data-ttu-id="73c2c-136">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="73c2c-136">OUTPUTS</span></span>

### <span data-ttu-id="73c2c-137">Microsoft. WindowsAzure. Management. ApplicationGateway. Models. ApplicationGatewayOperationResponse</span><span class="sxs-lookup"><span data-stu-id="73c2c-137">Microsoft.WindowsAzure.Management.ApplicationGateway.Models.ApplicationGatewayOperationResponse</span></span>

## <span data-ttu-id="73c2c-138">Пуск</span><span class="sxs-lookup"><span data-stu-id="73c2c-138">NOTES</span></span>

## <span data-ttu-id="73c2c-139">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="73c2c-139">RELATED LINKS</span></span>

[<span data-ttu-id="73c2c-140">Get-AzureApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="73c2c-140">Get-AzureApplicationGateway</span></span>](./Get-AzureApplicationGateway.md)

[<span data-ttu-id="73c2c-141">Remove-AzureApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="73c2c-141">Remove-AzureApplicationGateway</span></span>](./Remove-AzureApplicationGateway.md)

[<span data-ttu-id="73c2c-142">Start-AzureApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="73c2c-142">Start-AzureApplicationGateway</span></span>](./Start-AzureApplicationGateway.md)

[<span data-ttu-id="73c2c-143">Остановить-AzureApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="73c2c-143">Stop-AzureApplicationGateway</span></span>](./Stop-AzureApplicationGateway.md)

[<span data-ttu-id="73c2c-144">Update-AzureApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="73c2c-144">Update-AzureApplicationGateway</span></span>](./Update-AzureApplicationGateway.md)
