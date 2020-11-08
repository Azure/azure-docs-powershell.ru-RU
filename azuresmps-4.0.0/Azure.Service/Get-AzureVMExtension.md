---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 7ED074F0-1E9E-40C2-A543-D19A49831DD3
online version: ''
schema: 2.0.0
ms.openlocfilehash: 2f0b8ca9acfe5a62b002944bd44e11acfcd38ec1
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94076533"
---
# <span data-ttu-id="62a3f-101">Get-AzureVMExtension</span><span class="sxs-lookup"><span data-stu-id="62a3f-101">Get-AzureVMExtension</span></span>

## <span data-ttu-id="62a3f-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="62a3f-102">SYNOPSIS</span></span>
<span data-ttu-id="62a3f-103">Получение расширений ресурсов, примененных к виртуальным машинам.</span><span class="sxs-lookup"><span data-stu-id="62a3f-103">Gets resource extensions applied to virtual machines.</span></span>

## <span data-ttu-id="62a3f-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="62a3f-104">SYNTAX</span></span>

### <span data-ttu-id="62a3f-105">ListByReferenceName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="62a3f-105">ListByReferenceName (Default)</span></span>
```
Get-AzureVMExtension [[-ReferenceName] <String>] -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="62a3f-106">ListByExtensionName</span><span class="sxs-lookup"><span data-stu-id="62a3f-106">ListByExtensionName</span></span>
```
Get-AzureVMExtension [-ExtensionName] <String> [-Publisher] <String> [[-Version] <String>] -VM <IPersistentVM>
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

## <span data-ttu-id="62a3f-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="62a3f-107">DESCRIPTION</span></span>
<span data-ttu-id="62a3f-108">Командлет **Get-AzureVMExtension** получает расширения ресурсов, примененные к виртуальным машинам.</span><span class="sxs-lookup"><span data-stu-id="62a3f-108">The **Get-AzureVMExtension** cmdlet gets resource extensions applied to virtual machines.</span></span>

## <span data-ttu-id="62a3f-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="62a3f-109">EXAMPLES</span></span>

### <span data-ttu-id="62a3f-110">Пример 1: получение расширений ресурсов, примененных к виртуальной машине</span><span class="sxs-lookup"><span data-stu-id="62a3f-110">Example 1: Get the resource extensions applied to a virtual machine</span></span>
```
PS C:\> Get-AzureVM -ServiceName $SVC -Name $VM | Get-AzureVMExtension;
```

<span data-ttu-id="62a3f-111">Эта команда получает расширения ресурсов, примененные к указанной виртуальной машине, хранимой в $VM переменной.</span><span class="sxs-lookup"><span data-stu-id="62a3f-111">This command gets the resource extensions applied to the specified virtual machine as stored in the variable $VM.</span></span>

## <span data-ttu-id="62a3f-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="62a3f-112">PARAMETERS</span></span>

### <span data-ttu-id="62a3f-113">-ExtensionName</span><span class="sxs-lookup"><span data-stu-id="62a3f-113">-ExtensionName</span></span>
<span data-ttu-id="62a3f-114">Указывает имя расширения виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="62a3f-114">Specifies the virtual machine extension name.</span></span>

```yaml
Type: String
Parameter Sets: ListByExtensionName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="62a3f-115">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="62a3f-115">-InformationAction</span></span>
<span data-ttu-id="62a3f-116">Указывает, как этот командлет отвечает на информационное событие.</span><span class="sxs-lookup"><span data-stu-id="62a3f-116">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="62a3f-117">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="62a3f-117">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="62a3f-118">Продолжал</span><span class="sxs-lookup"><span data-stu-id="62a3f-118">Continue</span></span>
- <span data-ttu-id="62a3f-119">Игнорируйте</span><span class="sxs-lookup"><span data-stu-id="62a3f-119">Ignore</span></span>
- <span data-ttu-id="62a3f-120">INQUIRE</span><span class="sxs-lookup"><span data-stu-id="62a3f-120">Inquire</span></span>
- <span data-ttu-id="62a3f-121">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="62a3f-121">SilentlyContinue</span></span>
- <span data-ttu-id="62a3f-122">Остановить</span><span class="sxs-lookup"><span data-stu-id="62a3f-122">Stop</span></span>
- <span data-ttu-id="62a3f-123">Рвать</span><span class="sxs-lookup"><span data-stu-id="62a3f-123">Suspend</span></span>

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

### <span data-ttu-id="62a3f-124">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="62a3f-124">-InformationVariable</span></span>
<span data-ttu-id="62a3f-125">Указывает переменную данных.</span><span class="sxs-lookup"><span data-stu-id="62a3f-125">Specifies an information variable.</span></span>

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

### <span data-ttu-id="62a3f-126">-Profile</span><span class="sxs-lookup"><span data-stu-id="62a3f-126">-Profile</span></span>
<span data-ttu-id="62a3f-127">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="62a3f-127">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="62a3f-128">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="62a3f-128">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="62a3f-129">-Publisher</span><span class="sxs-lookup"><span data-stu-id="62a3f-129">-Publisher</span></span>
<span data-ttu-id="62a3f-130">Указывает издателя расширения.</span><span class="sxs-lookup"><span data-stu-id="62a3f-130">Specifies the publisher of the extension.</span></span>

```yaml
Type: String
Parameter Sets: ListByExtensionName
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="62a3f-131">-ReferenceName</span><span class="sxs-lookup"><span data-stu-id="62a3f-131">-ReferenceName</span></span>
<span data-ttu-id="62a3f-132">Указывает имя ссылки на расширение.</span><span class="sxs-lookup"><span data-stu-id="62a3f-132">Specifies the reference name of the extension.</span></span>

```yaml
Type: String
Parameter Sets: ListByReferenceName
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="62a3f-133">-Version</span><span class="sxs-lookup"><span data-stu-id="62a3f-133">-Version</span></span>
<span data-ttu-id="62a3f-134">Указывает версию расширения.</span><span class="sxs-lookup"><span data-stu-id="62a3f-134">Specifies the version of the extension.</span></span>

```yaml
Type: String
Parameter Sets: ListByExtensionName
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="62a3f-135">-VM</span><span class="sxs-lookup"><span data-stu-id="62a3f-135">-VM</span></span>
<span data-ttu-id="62a3f-136">Указывает Сохраняемый объект виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="62a3f-136">Specifies the persistent virtual machine object.</span></span>

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

### <span data-ttu-id="62a3f-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="62a3f-137">CommonParameters</span></span>
<span data-ttu-id="62a3f-138">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="62a3f-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="62a3f-139">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="62a3f-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="62a3f-140">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="62a3f-140">INPUTS</span></span>

## <span data-ttu-id="62a3f-141">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="62a3f-141">OUTPUTS</span></span>

## <span data-ttu-id="62a3f-142">Пуск</span><span class="sxs-lookup"><span data-stu-id="62a3f-142">NOTES</span></span>

## <span data-ttu-id="62a3f-143">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="62a3f-143">RELATED LINKS</span></span>

[<span data-ttu-id="62a3f-144">Remove-AzureVMExtension</span><span class="sxs-lookup"><span data-stu-id="62a3f-144">Remove-AzureVMExtension</span></span>](./Remove-AzureVMExtension.md)

[<span data-ttu-id="62a3f-145">Set-AzureVMExtension</span><span class="sxs-lookup"><span data-stu-id="62a3f-145">Set-AzureVMExtension</span></span>](./Set-AzureVMExtension.md)


