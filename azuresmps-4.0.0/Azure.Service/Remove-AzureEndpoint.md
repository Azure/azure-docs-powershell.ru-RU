---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 5A068EC9-3745-4219-BA03-C56CB9D9D157
online version: ''
schema: 2.0.0
ms.openlocfilehash: 24fad9fc499c3f7abec5e7539fd1e221835849ce
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94076478"
---
# <span data-ttu-id="f5219-101">Remove-AzureEndpoint</span><span class="sxs-lookup"><span data-stu-id="f5219-101">Remove-AzureEndpoint</span></span>

## <span data-ttu-id="f5219-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="f5219-102">SYNOPSIS</span></span>
<span data-ttu-id="f5219-103">Удаляет конечную точку из виртуальной машины Azure.</span><span class="sxs-lookup"><span data-stu-id="f5219-103">Deletes an endpoint from an Azure virtual machine.</span></span>

## <span data-ttu-id="f5219-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="f5219-104">SYNTAX</span></span>

```
Remove-AzureEndpoint [-Name] <String> -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="f5219-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f5219-105">DESCRIPTION</span></span>
<span data-ttu-id="f5219-106">Командлет **Remove-AzureEndpoint** удаляет конечную точку из объекта виртуальной машины Azure.</span><span class="sxs-lookup"><span data-stu-id="f5219-106">The **Remove-AzureEndpoint** cmdlet deletes an endpoint from an Azure virtual machine object.</span></span>

## <span data-ttu-id="f5219-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="f5219-107">EXAMPLES</span></span>

### <span data-ttu-id="f5219-108">Пример 1: Удаление конечной точки</span><span class="sxs-lookup"><span data-stu-id="f5219-108">Example 1: Remove an endpoint</span></span>
```
PS C:\> Get-AzureVM -ServiceName "ContosoService" -Name "VirtualMachine01" | Remove-AzureEndpoint -Name "HttpIn" | Update-AzureVM
```

<span data-ttu-id="f5219-109">Эта команда извлекает конфигурацию виртуальной машины с именем VirtualMachine01 с помощью командлета **Get-AzureVM** .</span><span class="sxs-lookup"><span data-stu-id="f5219-109">This command retrieves the configuration of a virtual machine named VirtualMachine01 by using the **Get-AzureVM** cmdlet.</span></span>
<span data-ttu-id="f5219-110">Команда передается текущему командлету с помощью оператора конвейера.</span><span class="sxs-lookup"><span data-stu-id="f5219-110">The command passes it to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="f5219-111">Этот командлет удаляет конечную точку с именем HTTP.</span><span class="sxs-lookup"><span data-stu-id="f5219-111">This cmdlet removes an endpoint named HttpIn.</span></span>
<span data-ttu-id="f5219-112">Команда передает объект виртуальной машины в командлет **Update-AzureVM** , который реализует ваши изменения.</span><span class="sxs-lookup"><span data-stu-id="f5219-112">The command passes the virtual machine object to the **Update-AzureVM** cmdlet, which implements your changes.</span></span>

## <span data-ttu-id="f5219-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="f5219-113">PARAMETERS</span></span>

### <span data-ttu-id="f5219-114">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="f5219-114">-InformationAction</span></span>
<span data-ttu-id="f5219-115">Указывает, как этот командлет отвечает на информационное событие.</span><span class="sxs-lookup"><span data-stu-id="f5219-115">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="f5219-116">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="f5219-116">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="f5219-117">Продолжал</span><span class="sxs-lookup"><span data-stu-id="f5219-117">Continue</span></span>
- <span data-ttu-id="f5219-118">Игнорируйте</span><span class="sxs-lookup"><span data-stu-id="f5219-118">Ignore</span></span>
- <span data-ttu-id="f5219-119">INQUIRE</span><span class="sxs-lookup"><span data-stu-id="f5219-119">Inquire</span></span>
- <span data-ttu-id="f5219-120">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="f5219-120">SilentlyContinue</span></span>
- <span data-ttu-id="f5219-121">Остановить</span><span class="sxs-lookup"><span data-stu-id="f5219-121">Stop</span></span>
- <span data-ttu-id="f5219-122">Рвать</span><span class="sxs-lookup"><span data-stu-id="f5219-122">Suspend</span></span>

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

### <span data-ttu-id="f5219-123">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="f5219-123">-InformationVariable</span></span>
<span data-ttu-id="f5219-124">Указывает переменную данных.</span><span class="sxs-lookup"><span data-stu-id="f5219-124">Specifies an information variable.</span></span>

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

### <span data-ttu-id="f5219-125">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="f5219-125">-Name</span></span>
<span data-ttu-id="f5219-126">Указывает имя конечной точки, которую этот командлет удаляет из виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="f5219-126">Specifies the name of the endpoint that this cmdlet deletes from the virtual machine.</span></span>

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

### <span data-ttu-id="f5219-127">-Profile</span><span class="sxs-lookup"><span data-stu-id="f5219-127">-Profile</span></span>
<span data-ttu-id="f5219-128">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="f5219-128">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="f5219-129">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="f5219-129">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="f5219-130">-VM</span><span class="sxs-lookup"><span data-stu-id="f5219-130">-VM</span></span>
<span data-ttu-id="f5219-131">Указывает виртуальную машину, из которой этот командлет удаляет конечную точку.</span><span class="sxs-lookup"><span data-stu-id="f5219-131">Specifies the virtual machine from which this cmdlet deletes an endpoint.</span></span>

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

### <span data-ttu-id="f5219-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f5219-132">CommonParameters</span></span>
<span data-ttu-id="f5219-133">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="f5219-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f5219-134">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f5219-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f5219-135">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="f5219-135">INPUTS</span></span>

## <span data-ttu-id="f5219-136">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="f5219-136">OUTPUTS</span></span>

## <span data-ttu-id="f5219-137">Пуск</span><span class="sxs-lookup"><span data-stu-id="f5219-137">NOTES</span></span>

## <span data-ttu-id="f5219-138">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f5219-138">RELATED LINKS</span></span>

[<span data-ttu-id="f5219-139">Add-AzureEndpoint</span><span class="sxs-lookup"><span data-stu-id="f5219-139">Add-AzureEndpoint</span></span>](./Add-AzureEndpoint.md)

[<span data-ttu-id="f5219-140">Get-AzureEndpoint</span><span class="sxs-lookup"><span data-stu-id="f5219-140">Get-AzureEndpoint</span></span>](./Get-AzureEndpoint.md)

[<span data-ttu-id="f5219-141">Get-AzureVM</span><span class="sxs-lookup"><span data-stu-id="f5219-141">Get-AzureVM</span></span>](./Get-AzureVM.md)

[<span data-ttu-id="f5219-142">Set-AzureEndpoint</span><span class="sxs-lookup"><span data-stu-id="f5219-142">Set-AzureEndpoint</span></span>](./Set-AzureEndpoint.md)

[<span data-ttu-id="f5219-143">Update-AzureVM</span><span class="sxs-lookup"><span data-stu-id="f5219-143">Update-AzureVM</span></span>](./Update-AzureVM.md)


