---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 1721107D-22FF-4A42-93C6-FD812DF81C33
online version: ''
schema: 2.0.0
ms.openlocfilehash: ac1bb63645b8db9e6a66971ad4ecd3b545a39100
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94076545"
---
# <span data-ttu-id="a2976-101">Get-AzureVMChefExtension</span><span class="sxs-lookup"><span data-stu-id="a2976-101">Get-AzureVMChefExtension</span></span>

## <span data-ttu-id="a2976-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="a2976-102">SYNOPSIS</span></span>
<span data-ttu-id="a2976-103">Получает расширение Chef, примененное на виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="a2976-103">Gets the Chef extension applied on a virtual machine.</span></span>

## <span data-ttu-id="a2976-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="a2976-104">SYNTAX</span></span>

```
Get-AzureVMChefExtension -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="a2976-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a2976-105">DESCRIPTION</span></span>
<span data-ttu-id="a2976-106">Командлет **Get-AzureVMChefExtension** получает расширение Chef, примененное на виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="a2976-106">The **Get-AzureVMChefExtension** cmdlet gets the Chef extension applied on a virtual machine.</span></span>

## <span data-ttu-id="a2976-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="a2976-107">EXAMPLES</span></span>

### <span data-ttu-id="a2976-108">Пример 1: получение расширения Chef, примененного на указанной виртуальной машине</span><span class="sxs-lookup"><span data-stu-id="a2976-108">Example 1: Get the Chef extension applied on the specified virtual machine</span></span>
```
PS C:\> Get-AzureVMChefExtension -VM $VM;
```

<span data-ttu-id="a2976-109">Эта команда получает расширение Chef, примененное к указанной виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="a2976-109">This command gets the Chef extension applied on the specified virtual machine.</span></span>

## <span data-ttu-id="a2976-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="a2976-110">PARAMETERS</span></span>

### <span data-ttu-id="a2976-111">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="a2976-111">-InformationAction</span></span>
<span data-ttu-id="a2976-112">Указывает, как этот командлет отвечает на информационное событие.</span><span class="sxs-lookup"><span data-stu-id="a2976-112">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="a2976-113">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="a2976-113">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="a2976-114">Продолжал</span><span class="sxs-lookup"><span data-stu-id="a2976-114">Continue</span></span>
- <span data-ttu-id="a2976-115">Игнорируйте</span><span class="sxs-lookup"><span data-stu-id="a2976-115">Ignore</span></span>
- <span data-ttu-id="a2976-116">INQUIRE</span><span class="sxs-lookup"><span data-stu-id="a2976-116">Inquire</span></span>
- <span data-ttu-id="a2976-117">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="a2976-117">SilentlyContinue</span></span>
- <span data-ttu-id="a2976-118">Остановить</span><span class="sxs-lookup"><span data-stu-id="a2976-118">Stop</span></span>
- <span data-ttu-id="a2976-119">Рвать</span><span class="sxs-lookup"><span data-stu-id="a2976-119">Suspend</span></span>

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

### <span data-ttu-id="a2976-120">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="a2976-120">-InformationVariable</span></span>
<span data-ttu-id="a2976-121">Указывает переменную данных.</span><span class="sxs-lookup"><span data-stu-id="a2976-121">Specifies an information variable.</span></span>

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

### <span data-ttu-id="a2976-122">-Profile</span><span class="sxs-lookup"><span data-stu-id="a2976-122">-Profile</span></span>
<span data-ttu-id="a2976-123">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="a2976-123">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="a2976-124">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="a2976-124">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="a2976-125">-VM</span><span class="sxs-lookup"><span data-stu-id="a2976-125">-VM</span></span>
<span data-ttu-id="a2976-126">Указывает Сохраняемый объект виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="a2976-126">Specifies the persistent virtual machine object.</span></span>

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

### <span data-ttu-id="a2976-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a2976-127">CommonParameters</span></span>
<span data-ttu-id="a2976-128">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="a2976-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a2976-129">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a2976-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a2976-130">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="a2976-130">INPUTS</span></span>

## <span data-ttu-id="a2976-131">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="a2976-131">OUTPUTS</span></span>

## <span data-ttu-id="a2976-132">Пуск</span><span class="sxs-lookup"><span data-stu-id="a2976-132">NOTES</span></span>

## <span data-ttu-id="a2976-133">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a2976-133">RELATED LINKS</span></span>

[<span data-ttu-id="a2976-134">Remove-AzureVMChefExtension</span><span class="sxs-lookup"><span data-stu-id="a2976-134">Remove-AzureVMChefExtension</span></span>](./Remove-AzureVMChefExtension.md)

[<span data-ttu-id="a2976-135">Set-AzureVMChefExtension</span><span class="sxs-lookup"><span data-stu-id="a2976-135">Set-AzureVMChefExtension</span></span>](./Set-AzureVMChefExtension.md)


