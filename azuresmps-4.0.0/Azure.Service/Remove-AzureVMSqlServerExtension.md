---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: C19A1DC0-47FA-4687-B81F-315EA04AD4A8
online version: ''
schema: 2.0.0
ms.openlocfilehash: 22591c1aa5a670e8f0d73f206ed6d2bcbe52c88f
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94075494"
---
# <span data-ttu-id="b94c5-101">Remove-AzureVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="b94c5-101">Remove-AzureVMSqlServerExtension</span></span>

## <span data-ttu-id="b94c5-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="b94c5-102">SYNOPSIS</span></span>
<span data-ttu-id="b94c5-103">Удаляет расширение SQL Server виртуальной машины Azure из объекта виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="b94c5-103">Removes an Azure virtual machine SQL Server extension from a virtual machine object.</span></span>

## <span data-ttu-id="b94c5-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="b94c5-104">SYNTAX</span></span>

```
Remove-AzureVMSqlServerExtension -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="b94c5-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b94c5-105">DESCRIPTION</span></span>
<span data-ttu-id="b94c5-106">Командлет **Remove-AzureVMSqlServerExtension** УДАЛЯЕТ расширение SQL Server виртуальной машины Azure из объекта виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="b94c5-106">The **Remove-AzureVMSqlServerExtension** cmdlet removes an Azure virtual machine SQL Server extension from a virtual machine object.</span></span>

## <span data-ttu-id="b94c5-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="b94c5-107">EXAMPLES</span></span>

### <span data-ttu-id="b94c5-108">1:</span><span class="sxs-lookup"><span data-stu-id="b94c5-108">1:</span></span>
```

```

## <span data-ttu-id="b94c5-109">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="b94c5-109">PARAMETERS</span></span>

### <span data-ttu-id="b94c5-110">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="b94c5-110">-InformationAction</span></span>
<span data-ttu-id="b94c5-111">Указывает, как этот командлет отвечает на информационное событие.</span><span class="sxs-lookup"><span data-stu-id="b94c5-111">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="b94c5-112">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="b94c5-112">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="b94c5-113">Продолжал</span><span class="sxs-lookup"><span data-stu-id="b94c5-113">Continue</span></span>
- <span data-ttu-id="b94c5-114">Игнорируйте</span><span class="sxs-lookup"><span data-stu-id="b94c5-114">Ignore</span></span>
- <span data-ttu-id="b94c5-115">INQUIRE</span><span class="sxs-lookup"><span data-stu-id="b94c5-115">Inquire</span></span>
- <span data-ttu-id="b94c5-116">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="b94c5-116">SilentlyContinue</span></span>
- <span data-ttu-id="b94c5-117">Остановить</span><span class="sxs-lookup"><span data-stu-id="b94c5-117">Stop</span></span>
- <span data-ttu-id="b94c5-118">Рвать</span><span class="sxs-lookup"><span data-stu-id="b94c5-118">Suspend</span></span>

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

### <span data-ttu-id="b94c5-119">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="b94c5-119">-InformationVariable</span></span>
<span data-ttu-id="b94c5-120">Указывает переменную данных.</span><span class="sxs-lookup"><span data-stu-id="b94c5-120">Specifies an information variable.</span></span>

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

### <span data-ttu-id="b94c5-121">-Profile</span><span class="sxs-lookup"><span data-stu-id="b94c5-121">-Profile</span></span>
<span data-ttu-id="b94c5-122">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="b94c5-122">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="b94c5-123">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="b94c5-123">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="b94c5-124">-VM</span><span class="sxs-lookup"><span data-stu-id="b94c5-124">-VM</span></span>
<span data-ttu-id="b94c5-125">Указывает Сохраняемый объект виртуальной машины, из которого этот командлет удаляет расширение.</span><span class="sxs-lookup"><span data-stu-id="b94c5-125">Specifies the persistent virtual machine object that this cmdlet removes the extension from.</span></span>

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

### <span data-ttu-id="b94c5-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b94c5-126">CommonParameters</span></span>
<span data-ttu-id="b94c5-127">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="b94c5-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b94c5-128">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b94c5-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b94c5-129">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="b94c5-129">INPUTS</span></span>

## <span data-ttu-id="b94c5-130">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="b94c5-130">OUTPUTS</span></span>

## <span data-ttu-id="b94c5-131">Пуск</span><span class="sxs-lookup"><span data-stu-id="b94c5-131">NOTES</span></span>

## <span data-ttu-id="b94c5-132">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b94c5-132">RELATED LINKS</span></span>

[<span data-ttu-id="b94c5-133">Get-AzureVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="b94c5-133">Get-AzureVMSqlServerExtension</span></span>](./Get-AzureVMSqlServerExtension.md)

[<span data-ttu-id="b94c5-134">Set-AzureVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="b94c5-134">Set-AzureVMSqlServerExtension</span></span>](./Set-AzureVMSqlServerExtension.md)


