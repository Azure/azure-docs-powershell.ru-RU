---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 9EA98944-1923-4573-991E-3B9CA21004BB
online version: ''
schema: 2.0.0
ms.openlocfilehash: 2f16b51dc8abf5c6243b4b489789d65029acc3c4
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94076148"
---
# <span data-ttu-id="123b7-101">Remove-AzurePublicIP</span><span class="sxs-lookup"><span data-stu-id="123b7-101">Remove-AzurePublicIP</span></span>

## <span data-ttu-id="123b7-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="123b7-102">SYNOPSIS</span></span>
<span data-ttu-id="123b7-103">Удаление общедоступной конфигурации IP с виртуальной машины Azure.</span><span class="sxs-lookup"><span data-stu-id="123b7-103">Removes Public IP configuration from an Azure virtual machine.</span></span>

## <span data-ttu-id="123b7-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="123b7-104">SYNTAX</span></span>

```
Remove-AzurePublicIP [[-PublicIPName] <String>] -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="123b7-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="123b7-105">DESCRIPTION</span></span>
<span data-ttu-id="123b7-106">Командлет **Remove-AzurePublicIP** удаляет общедоступную конфигурацию IP-адресов из виртуальной машины Azure.</span><span class="sxs-lookup"><span data-stu-id="123b7-106">The **Remove-AzurePublicIP** cmdlet removes Public IP configuration from an Azure virtual machine.</span></span>

## <span data-ttu-id="123b7-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="123b7-107">EXAMPLES</span></span>

### <span data-ttu-id="123b7-108">Пример 1: удаление общедоступной конфигурации IP</span><span class="sxs-lookup"><span data-stu-id="123b7-108">Example 1: Remove Public IP configuration</span></span>
```
PS C:\> Get-AzureVM -ServiceName "FTPInAzure" -Name "FTPInstance" | Remove-AzurePublicIP | Update-AzureVM
```

<span data-ttu-id="123b7-109">Эта команда получает виртуальную машину с именем FTPInstance в службе с именем FTPInAzure с помощью командлета **Get-AzureVM** .</span><span class="sxs-lookup"><span data-stu-id="123b7-109">This command gets the virtual machine named FTPInstance in the service named FTPInAzure by using the **Get-AzureVM** cmdlet.</span></span>
<span data-ttu-id="123b7-110">Команда передает эту виртуальную машину в текущий командлет с помощью оператора конвейера.</span><span class="sxs-lookup"><span data-stu-id="123b7-110">The command passes that virtual machine to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="123b7-111">Текущий командлет удаляет общедоступную IP-конфигурацию из виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="123b7-111">The current cmdlet removes Public IP configuration from the virtual machine.</span></span>
<span data-ttu-id="123b7-112">Команда передает виртуальную машину командлету **Update-AzureVM** , который реализует ваши изменения.</span><span class="sxs-lookup"><span data-stu-id="123b7-112">The command passes the virtual machine to the **Update-AzureVM** cmdlet, which implements your changes.</span></span>

## <span data-ttu-id="123b7-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="123b7-113">PARAMETERS</span></span>

### <span data-ttu-id="123b7-114">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="123b7-114">-InformationAction</span></span>
<span data-ttu-id="123b7-115">Указывает, как этот командлет отвечает на информационное событие.</span><span class="sxs-lookup"><span data-stu-id="123b7-115">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="123b7-116">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="123b7-116">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="123b7-117">Продолжал</span><span class="sxs-lookup"><span data-stu-id="123b7-117">Continue</span></span>
- <span data-ttu-id="123b7-118">Игнорируйте</span><span class="sxs-lookup"><span data-stu-id="123b7-118">Ignore</span></span>
- <span data-ttu-id="123b7-119">INQUIRE</span><span class="sxs-lookup"><span data-stu-id="123b7-119">Inquire</span></span>
- <span data-ttu-id="123b7-120">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="123b7-120">SilentlyContinue</span></span>
- <span data-ttu-id="123b7-121">Остановить</span><span class="sxs-lookup"><span data-stu-id="123b7-121">Stop</span></span>
- <span data-ttu-id="123b7-122">Рвать</span><span class="sxs-lookup"><span data-stu-id="123b7-122">Suspend</span></span>

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

### <span data-ttu-id="123b7-123">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="123b7-123">-InformationVariable</span></span>
<span data-ttu-id="123b7-124">Указывает переменную данных.</span><span class="sxs-lookup"><span data-stu-id="123b7-124">Specifies an information variable.</span></span>

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

### <span data-ttu-id="123b7-125">-Profile</span><span class="sxs-lookup"><span data-stu-id="123b7-125">-Profile</span></span>
<span data-ttu-id="123b7-126">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="123b7-126">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="123b7-127">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="123b7-127">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="123b7-128">-PublicIPName</span><span class="sxs-lookup"><span data-stu-id="123b7-128">-PublicIPName</span></span>
<span data-ttu-id="123b7-129">Указывает общедоступное имя IP-адреса.</span><span class="sxs-lookup"><span data-stu-id="123b7-129">Specifies the Public IP name.</span></span>

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

### <span data-ttu-id="123b7-130">-VM</span><span class="sxs-lookup"><span data-stu-id="123b7-130">-VM</span></span>
<span data-ttu-id="123b7-131">Указывает виртуальную машину, с которой этот командлет удаляет общедоступную конфигурацию IP-адресов.</span><span class="sxs-lookup"><span data-stu-id="123b7-131">Specifies the virtual machine from which this cmdlet removes Public IP configuration.</span></span>

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

### <span data-ttu-id="123b7-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="123b7-132">CommonParameters</span></span>
<span data-ttu-id="123b7-133">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="123b7-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="123b7-134">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="123b7-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="123b7-135">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="123b7-135">INPUTS</span></span>

## <span data-ttu-id="123b7-136">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="123b7-136">OUTPUTS</span></span>

### <span data-ttu-id="123b7-137">Microsoft. WindowsAzure. Commands. ServiceManagement. Model. IPersistentVM</span><span class="sxs-lookup"><span data-stu-id="123b7-137">Microsoft.WindowsAzure.Commands.ServiceManagement.Model.IPersistentVM</span></span>

## <span data-ttu-id="123b7-138">Пуск</span><span class="sxs-lookup"><span data-stu-id="123b7-138">NOTES</span></span>

## <span data-ttu-id="123b7-139">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="123b7-139">RELATED LINKS</span></span>

[<span data-ttu-id="123b7-140">Get-AzurePublicIP</span><span class="sxs-lookup"><span data-stu-id="123b7-140">Get-AzurePublicIP</span></span>](./Get-AzurePublicIP.md)

[<span data-ttu-id="123b7-141">Get-AzureVM</span><span class="sxs-lookup"><span data-stu-id="123b7-141">Get-AzureVM</span></span>](./Get-AzureVM.md)

[<span data-ttu-id="123b7-142">Set-AzurePublicIP</span><span class="sxs-lookup"><span data-stu-id="123b7-142">Set-AzurePublicIP</span></span>](./Set-AzurePublicIP.md)

[<span data-ttu-id="123b7-143">Update-AzureVM</span><span class="sxs-lookup"><span data-stu-id="123b7-143">Update-AzureVM</span></span>](./Update-AzureVM.md)


