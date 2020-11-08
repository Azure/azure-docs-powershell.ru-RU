---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 9AC28E79-0E3F-4AED-8BFE-8D1C4DCB7715
online version: ''
schema: 2.0.0
ms.openlocfilehash: fd7ece4f8f414df7be6e2d38920f516119f4b82a
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94076526"
---
# <span data-ttu-id="2baf1-101">Get-AzureVMPuppetExtension</span><span class="sxs-lookup"><span data-stu-id="2baf1-101">Get-AzureVMPuppetExtension</span></span>

## <span data-ttu-id="2baf1-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="2baf1-102">SYNOPSIS</span></span>
<span data-ttu-id="2baf1-103">Получает расширение Puppet, примененное на виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="2baf1-103">Gets the Puppet extension applied on a virtual machine.</span></span>

## <span data-ttu-id="2baf1-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="2baf1-104">SYNTAX</span></span>

```
Get-AzureVMPuppetExtension -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="2baf1-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="2baf1-105">DESCRIPTION</span></span>
<span data-ttu-id="2baf1-106">Командлет **Get-AzureVMPuppetExtension** получает расширение Puppet, примененное на виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="2baf1-106">The **Get-AzureVMPuppetExtension** cmdlet gets the Puppet extension applied on a virtual machine.</span></span>

## <span data-ttu-id="2baf1-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="2baf1-107">EXAMPLES</span></span>

### <span data-ttu-id="2baf1-108">Пример 1: получение расширения Puppet, примененного на виртуальной машине</span><span class="sxs-lookup"><span data-stu-id="2baf1-108">Example 1: Get the Puppet extension applied on a virtual machine</span></span>
```
PS C:\> Get-AzureVMPuppetExtension -VM $VM
```

<span data-ttu-id="2baf1-109">Эта команда получает расширение Puppet, примененное на виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="2baf1-109">This command gets the Puppet extension applied on a virtual machine.</span></span>

## <span data-ttu-id="2baf1-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="2baf1-110">PARAMETERS</span></span>

### <span data-ttu-id="2baf1-111">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="2baf1-111">-InformationAction</span></span>
<span data-ttu-id="2baf1-112">Указывает, как этот командлет отвечает на информационное событие.</span><span class="sxs-lookup"><span data-stu-id="2baf1-112">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="2baf1-113">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="2baf1-113">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="2baf1-114">Продолжал</span><span class="sxs-lookup"><span data-stu-id="2baf1-114">Continue</span></span>
- <span data-ttu-id="2baf1-115">Игнорируйте</span><span class="sxs-lookup"><span data-stu-id="2baf1-115">Ignore</span></span>
- <span data-ttu-id="2baf1-116">INQUIRE</span><span class="sxs-lookup"><span data-stu-id="2baf1-116">Inquire</span></span>
- <span data-ttu-id="2baf1-117">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="2baf1-117">SilentlyContinue</span></span>
- <span data-ttu-id="2baf1-118">Остановить</span><span class="sxs-lookup"><span data-stu-id="2baf1-118">Stop</span></span>
- <span data-ttu-id="2baf1-119">Рвать</span><span class="sxs-lookup"><span data-stu-id="2baf1-119">Suspend</span></span>

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

### <span data-ttu-id="2baf1-120">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="2baf1-120">-InformationVariable</span></span>
<span data-ttu-id="2baf1-121">Указывает переменную данных.</span><span class="sxs-lookup"><span data-stu-id="2baf1-121">Specifies an information variable.</span></span>

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

### <span data-ttu-id="2baf1-122">-Profile</span><span class="sxs-lookup"><span data-stu-id="2baf1-122">-Profile</span></span>
<span data-ttu-id="2baf1-123">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="2baf1-123">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="2baf1-124">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="2baf1-124">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="2baf1-125">-VM</span><span class="sxs-lookup"><span data-stu-id="2baf1-125">-VM</span></span>
<span data-ttu-id="2baf1-126">Указывает Сохраняемый объект виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="2baf1-126">Specifies the persistent virtual machine object.</span></span>

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

### <span data-ttu-id="2baf1-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2baf1-127">CommonParameters</span></span>
<span data-ttu-id="2baf1-128">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="2baf1-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2baf1-129">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2baf1-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2baf1-130">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="2baf1-130">INPUTS</span></span>

## <span data-ttu-id="2baf1-131">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="2baf1-131">OUTPUTS</span></span>

## <span data-ttu-id="2baf1-132">Пуск</span><span class="sxs-lookup"><span data-stu-id="2baf1-132">NOTES</span></span>

## <span data-ttu-id="2baf1-133">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="2baf1-133">RELATED LINKS</span></span>

[<span data-ttu-id="2baf1-134">Remove-AzureVMPuppetExtension</span><span class="sxs-lookup"><span data-stu-id="2baf1-134">Remove-AzureVMPuppetExtension</span></span>](./Remove-AzureVMPuppetExtension.md)

[<span data-ttu-id="2baf1-135">Set-AzureVMPuppetExtension</span><span class="sxs-lookup"><span data-stu-id="2baf1-135">Set-AzureVMPuppetExtension</span></span>](./Set-AzureVMPuppetExtension.md)


