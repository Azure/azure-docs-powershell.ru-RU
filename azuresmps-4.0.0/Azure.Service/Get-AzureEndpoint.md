---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 1CFB90FD-7BC5-4687-8D08-775097DDA062
online version: ''
schema: 2.0.0
ms.openlocfilehash: 651b38a21dff03ce3c5925040d65bc2967eeaa77
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94075645"
---
# <span data-ttu-id="86371-101">Get-AzureEndpoint</span><span class="sxs-lookup"><span data-stu-id="86371-101">Get-AzureEndpoint</span></span>

## <span data-ttu-id="86371-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="86371-102">SYNOPSIS</span></span>
<span data-ttu-id="86371-103">Получение сведений о конечных точках, назначенных виртуальной машине Azure.</span><span class="sxs-lookup"><span data-stu-id="86371-103">Gets information about the endpoints that are assigned to an Azure virtual machine.</span></span>

## <span data-ttu-id="86371-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="86371-104">SYNTAX</span></span>

```
Get-AzureEndpoint [[-Name] <String>] -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="86371-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="86371-105">DESCRIPTION</span></span>
<span data-ttu-id="86371-106">Командлет **Get-AzureEndpoint** получает сведения о конечных точках, которые назначены виртуальной машине Azure.</span><span class="sxs-lookup"><span data-stu-id="86371-106">The **Get-AzureEndpoint** cmdlet gets information about the endpoints that are assigned to an Azure virtual machine.</span></span>

## <span data-ttu-id="86371-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="86371-107">EXAMPLES</span></span>

### <span data-ttu-id="86371-108">Пример 1: получение сведений о конечной точке для виртуальной машины</span><span class="sxs-lookup"><span data-stu-id="86371-108">Example 1: Get endpoint information for a virtual machine</span></span>
```
PS C:\> Get-AzureVM -ServiceName "ContosoService" -Name "VirtualMachine12" | Get-AzureEndpoint
```

<span data-ttu-id="86371-109">Эта команда извлекает конфигурацию виртуальной машины с именем VirtualMachine12 с помощью командлета **Get-AzureVM** .</span><span class="sxs-lookup"><span data-stu-id="86371-109">This command retrieves the configuration of a virtual machine named VirtualMachine12 by using the **Get-AzureVM** cmdlet.</span></span>
<span data-ttu-id="86371-110">Команда передается текущему командлету с помощью оператора конвейера.</span><span class="sxs-lookup"><span data-stu-id="86371-110">The command passes it to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="86371-111">Этот командлет получает сведения о конечной точке для этой виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="86371-111">This cmdlet gets endpoint information for that virtual machine.</span></span>

## <span data-ttu-id="86371-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="86371-112">PARAMETERS</span></span>

### <span data-ttu-id="86371-113">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="86371-113">-InformationAction</span></span>
<span data-ttu-id="86371-114">Указывает, как этот командлет отвечает на информационное событие.</span><span class="sxs-lookup"><span data-stu-id="86371-114">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="86371-115">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="86371-115">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="86371-116">Продолжал</span><span class="sxs-lookup"><span data-stu-id="86371-116">Continue</span></span>
- <span data-ttu-id="86371-117">Игнорируйте</span><span class="sxs-lookup"><span data-stu-id="86371-117">Ignore</span></span>
- <span data-ttu-id="86371-118">INQUIRE</span><span class="sxs-lookup"><span data-stu-id="86371-118">Inquire</span></span>
- <span data-ttu-id="86371-119">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="86371-119">SilentlyContinue</span></span>
- <span data-ttu-id="86371-120">Остановить</span><span class="sxs-lookup"><span data-stu-id="86371-120">Stop</span></span>
- <span data-ttu-id="86371-121">Рвать</span><span class="sxs-lookup"><span data-stu-id="86371-121">Suspend</span></span>

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

### <span data-ttu-id="86371-122">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="86371-122">-InformationVariable</span></span>
<span data-ttu-id="86371-123">Указывает переменную данных.</span><span class="sxs-lookup"><span data-stu-id="86371-123">Specifies an information variable.</span></span>

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

### <span data-ttu-id="86371-124">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="86371-124">-Name</span></span>
<span data-ttu-id="86371-125">Указывает имя конечной точки, для которой этот командлет получает сведения.</span><span class="sxs-lookup"><span data-stu-id="86371-125">Specifies the name of the endpoint for which this cmdlet gets information.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="86371-126">-Profile</span><span class="sxs-lookup"><span data-stu-id="86371-126">-Profile</span></span>
<span data-ttu-id="86371-127">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="86371-127">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="86371-128">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="86371-128">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="86371-129">-VM</span><span class="sxs-lookup"><span data-stu-id="86371-129">-VM</span></span>
<span data-ttu-id="86371-130">Указывает виртуальную машину, с которой этот командлет получает сведения о конечной точке.</span><span class="sxs-lookup"><span data-stu-id="86371-130">Specifies the virtual machine from which this cmdlet gets endpoint information.</span></span>

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

### <span data-ttu-id="86371-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="86371-131">CommonParameters</span></span>
<span data-ttu-id="86371-132">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="86371-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="86371-133">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="86371-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="86371-134">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="86371-134">INPUTS</span></span>

## <span data-ttu-id="86371-135">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="86371-135">OUTPUTS</span></span>

## <span data-ttu-id="86371-136">Пуск</span><span class="sxs-lookup"><span data-stu-id="86371-136">NOTES</span></span>

## <span data-ttu-id="86371-137">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="86371-137">RELATED LINKS</span></span>

[<span data-ttu-id="86371-138">Add-AzureEndpoint</span><span class="sxs-lookup"><span data-stu-id="86371-138">Add-AzureEndpoint</span></span>](./Add-AzureEndpoint.md)

[<span data-ttu-id="86371-139">Get-AzureVM</span><span class="sxs-lookup"><span data-stu-id="86371-139">Get-AzureVM</span></span>](./Get-AzureVM.md)

[<span data-ttu-id="86371-140">Remove-AzureEndpoint</span><span class="sxs-lookup"><span data-stu-id="86371-140">Remove-AzureEndpoint</span></span>](./Remove-AzureEndpoint.md)

[<span data-ttu-id="86371-141">Set-AzureEndpoint</span><span class="sxs-lookup"><span data-stu-id="86371-141">Set-AzureEndpoint</span></span>](./Set-AzureEndpoint.md)


