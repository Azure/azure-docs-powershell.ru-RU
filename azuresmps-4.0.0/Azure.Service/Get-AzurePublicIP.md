---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 5BEE9430-D6BF-49F1-A23D-32784C6C818E
online version: ''
schema: 2.0.0
ms.openlocfilehash: 98b9abe6bcb9998067fe978a5f99f5d8b64cd26d
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94076331"
---
# <span data-ttu-id="8f915-101">Get-AzurePublicIP</span><span class="sxs-lookup"><span data-stu-id="8f915-101">Get-AzurePublicIP</span></span>

## <span data-ttu-id="8f915-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="8f915-102">SYNOPSIS</span></span>
<span data-ttu-id="8f915-103">Получает общедоступные IP-сведения для виртуальной машины Azure.</span><span class="sxs-lookup"><span data-stu-id="8f915-103">Gets the Public IP information for an Azure virtual machine.</span></span>

## <span data-ttu-id="8f915-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="8f915-104">SYNTAX</span></span>

```
Get-AzurePublicIP [[-PublicIPName] <String>] -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="8f915-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="8f915-105">DESCRIPTION</span></span>
<span data-ttu-id="8f915-106">Командлет **Get-AzurePublicIP** получает общедоступные IP-сведения для виртуальной машины Azure.</span><span class="sxs-lookup"><span data-stu-id="8f915-106">The **Get-AzurePublicIP** cmdlet gets the Public IP information for an Azure virtual machine.</span></span>
<span data-ttu-id="8f915-107">Чтобы получить IP-адрес общедоступного IP-адреса, используйте командлет **Get-AzureVM** .</span><span class="sxs-lookup"><span data-stu-id="8f915-107">To obtain the IP address of the Public IP, use the **Get-AzureVM** cmdlet.</span></span>

## <span data-ttu-id="8f915-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="8f915-108">EXAMPLES</span></span>

### <span data-ttu-id="8f915-109">Пример 1: получение общедоступной конфигурации IP</span><span class="sxs-lookup"><span data-stu-id="8f915-109">Example 1: Get Public IP configuration</span></span>
```
PS C:\> Get-AzureVM -ServiceName "FTPInAzure" -Name "FTPInstance" | Get-AzurePublicIP
```

<span data-ttu-id="8f915-110">Эта команда получает виртуальную машину с именем FTPInstance в службе с именем FTPInAzure с помощью командлета **Get-AzureVM** .</span><span class="sxs-lookup"><span data-stu-id="8f915-110">This command gets the virtual machine named FTPInstance in the service named FTPInAzure by using the **Get-AzureVM** cmdlet.</span></span>
<span data-ttu-id="8f915-111">Команда передает эту виртуальную машину в текущий командлет с помощью оператора конвейера.</span><span class="sxs-lookup"><span data-stu-id="8f915-111">The command passes that virtual machine to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="8f915-112">Текущий командлет получает общедоступную IP-конфигурацию из виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="8f915-112">The current cmdlet gets Public IP configuration from the virtual machine.</span></span>

## <span data-ttu-id="8f915-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="8f915-113">PARAMETERS</span></span>

### <span data-ttu-id="8f915-114">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="8f915-114">-InformationAction</span></span>
<span data-ttu-id="8f915-115">Указывает, как этот командлет отвечает на информационное событие.</span><span class="sxs-lookup"><span data-stu-id="8f915-115">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="8f915-116">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="8f915-116">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="8f915-117">Продолжал</span><span class="sxs-lookup"><span data-stu-id="8f915-117">Continue</span></span>
- <span data-ttu-id="8f915-118">Игнорируйте</span><span class="sxs-lookup"><span data-stu-id="8f915-118">Ignore</span></span>
- <span data-ttu-id="8f915-119">INQUIRE</span><span class="sxs-lookup"><span data-stu-id="8f915-119">Inquire</span></span>
- <span data-ttu-id="8f915-120">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="8f915-120">SilentlyContinue</span></span>
- <span data-ttu-id="8f915-121">Остановить</span><span class="sxs-lookup"><span data-stu-id="8f915-121">Stop</span></span>
- <span data-ttu-id="8f915-122">Рвать</span><span class="sxs-lookup"><span data-stu-id="8f915-122">Suspend</span></span>

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

### <span data-ttu-id="8f915-123">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="8f915-123">-InformationVariable</span></span>
<span data-ttu-id="8f915-124">Указывает переменную данных.</span><span class="sxs-lookup"><span data-stu-id="8f915-124">Specifies an information variable.</span></span>

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

### <span data-ttu-id="8f915-125">-Profile</span><span class="sxs-lookup"><span data-stu-id="8f915-125">-Profile</span></span>
<span data-ttu-id="8f915-126">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="8f915-126">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="8f915-127">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="8f915-127">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="8f915-128">-PublicIPName</span><span class="sxs-lookup"><span data-stu-id="8f915-128">-PublicIPName</span></span>
<span data-ttu-id="8f915-129">Указывает общедоступное имя IP-адреса.</span><span class="sxs-lookup"><span data-stu-id="8f915-129">Specifies the Public IP name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8f915-130">-VM</span><span class="sxs-lookup"><span data-stu-id="8f915-130">-VM</span></span>
<span data-ttu-id="8f915-131">Указывает виртуальную машину, для которой этот командлет получает общедоступную конфигурацию IP-адресов.</span><span class="sxs-lookup"><span data-stu-id="8f915-131">Specifies the virtual machine for which this cmdlet gets Public IP configuration.</span></span>

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

### <span data-ttu-id="8f915-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8f915-132">CommonParameters</span></span>
<span data-ttu-id="8f915-133">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="8f915-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8f915-134">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8f915-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8f915-135">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="8f915-135">INPUTS</span></span>

## <span data-ttu-id="8f915-136">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="8f915-136">OUTPUTS</span></span>

### <span data-ttu-id="8f915-137">Microsoft. WindowsAzure. Commands. ServiceManagement. AssignPublicIPCollection</span><span class="sxs-lookup"><span data-stu-id="8f915-137">Microsoft.WindowsAzure.Commands.ServiceManagement.AssignPublicIPCollection</span></span>

## <span data-ttu-id="8f915-138">Пуск</span><span class="sxs-lookup"><span data-stu-id="8f915-138">NOTES</span></span>

## <span data-ttu-id="8f915-139">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="8f915-139">RELATED LINKS</span></span>

[<span data-ttu-id="8f915-140">Get-AzureVM</span><span class="sxs-lookup"><span data-stu-id="8f915-140">Get-AzureVM</span></span>](./Get-AzureVM.md)

[<span data-ttu-id="8f915-141">Remove-AzurePublicIP</span><span class="sxs-lookup"><span data-stu-id="8f915-141">Remove-AzurePublicIP</span></span>](./Remove-AzurePublicIP.md)

[<span data-ttu-id="8f915-142">Set-AzurePublicIP</span><span class="sxs-lookup"><span data-stu-id="8f915-142">Set-AzurePublicIP</span></span>](./Set-AzurePublicIP.md)


