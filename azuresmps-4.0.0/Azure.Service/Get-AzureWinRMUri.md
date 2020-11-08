---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 5F827BFB-492E-48A2-9610-0CB5FBDD1F9E
online version: ''
schema: 2.0.0
ms.openlocfilehash: 0c66043fa36620c2879e88b7dbf82ba251aa4fbc
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94076505"
---
# <span data-ttu-id="84e38-101">Get-AzureWinRMUri</span><span class="sxs-lookup"><span data-stu-id="84e38-101">Get-AzureWinRMUri</span></span>

## <span data-ttu-id="84e38-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="84e38-102">SYNOPSIS</span></span>
<span data-ttu-id="84e38-103">Получает универсальный код ресурса (URI) для удаленного прослушивателя HTTPS на виртуальную машину или список виртуальных машин в размещенной службе.</span><span class="sxs-lookup"><span data-stu-id="84e38-103">Gets the URI to WinRM https listener to a virtual machine or a list of virtual machines in a hosted service.</span></span>

## <span data-ttu-id="84e38-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="84e38-104">SYNTAX</span></span>

```
Get-AzureWinRMUri [-ServiceName] <String> [[-Name] <String>] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="84e38-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="84e38-105">DESCRIPTION</span></span>
<span data-ttu-id="84e38-106">Командлет **Get-AzureWinRMUri** возвращает универсальный код ресурса (URI) прослушивателя HTTPS для удаленного управления Windows (WinRM) на виртуальную машину или список виртуальных машин в размещенной службе.</span><span class="sxs-lookup"><span data-stu-id="84e38-106">The **Get-AzureWinRMUri** cmdlet gets the URI of the Windows Remote Management (WinRM) https listener to a virtual machine or a list of virtual machines in a hosted service.</span></span>

## <span data-ttu-id="84e38-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="84e38-107">EXAMPLES</span></span>

### <span data-ttu-id="84e38-108">Пример 1: Получение URI-кода прослушивателя WinRM HTTPS для виртуальной машины</span><span class="sxs-lookup"><span data-stu-id="84e38-108">Example 1: Get the URI of the WinRM https listener to a virtual machine</span></span>
```
PS C:\> Get-AzureWinRMUri -ServiceName MyService -Name MyVM
```

<span data-ttu-id="84e38-109">Эта команда возвращает UIR прослушивателя HTTPS для WinRM на виртуальную машину.</span><span class="sxs-lookup"><span data-stu-id="84e38-109">This command gets the UIR of the WinRM https listener to a virtual machine.</span></span>

### <span data-ttu-id="84e38-110">Пример 2: Получение URI-кода прослушивателя WinRM HTTPS для виртуальной машины определенной службы</span><span class="sxs-lookup"><span data-stu-id="84e38-110">Example 2: Get the URI of the WinRM https listener to a virtual machine of a specific service</span></span>
```
PS C:\> Get-AzureWinRMUri -ServiceName MyService
```

<span data-ttu-id="84e38-111">Эта команда возвращает UIR прослушивателя HTTPS для WinRM на виртуальную машину.</span><span class="sxs-lookup"><span data-stu-id="84e38-111">This command gets the UIR of the WinRM https listener to a virtual machine.</span></span>

## <span data-ttu-id="84e38-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="84e38-112">PARAMETERS</span></span>

### <span data-ttu-id="84e38-113">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="84e38-113">-InformationAction</span></span>
<span data-ttu-id="84e38-114">Указывает, как этот командлет отвечает на информационное событие.</span><span class="sxs-lookup"><span data-stu-id="84e38-114">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="84e38-115">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="84e38-115">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="84e38-116">Продолжал</span><span class="sxs-lookup"><span data-stu-id="84e38-116">Continue</span></span>
- <span data-ttu-id="84e38-117">Игнорируйте</span><span class="sxs-lookup"><span data-stu-id="84e38-117">Ignore</span></span>
- <span data-ttu-id="84e38-118">INQUIRE</span><span class="sxs-lookup"><span data-stu-id="84e38-118">Inquire</span></span>
- <span data-ttu-id="84e38-119">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="84e38-119">SilentlyContinue</span></span>
- <span data-ttu-id="84e38-120">Остановить</span><span class="sxs-lookup"><span data-stu-id="84e38-120">Stop</span></span>
- <span data-ttu-id="84e38-121">Рвать</span><span class="sxs-lookup"><span data-stu-id="84e38-121">Suspend</span></span>

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

### <span data-ttu-id="84e38-122">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="84e38-122">-InformationVariable</span></span>
<span data-ttu-id="84e38-123">Указывает переменную данных.</span><span class="sxs-lookup"><span data-stu-id="84e38-123">Specifies an information variable.</span></span>

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

### <span data-ttu-id="84e38-124">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="84e38-124">-Name</span></span>
<span data-ttu-id="84e38-125">Указывает имя виртуальной машины, для которой создается универсальный код ресурса (URI) WinRM.</span><span class="sxs-lookup"><span data-stu-id="84e38-125">Specifies the name of the virtual machine to which the WinRM URI is generated.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="84e38-126">-Profile</span><span class="sxs-lookup"><span data-stu-id="84e38-126">-Profile</span></span>
<span data-ttu-id="84e38-127">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="84e38-127">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="84e38-128">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="84e38-128">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="84e38-129">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="84e38-129">-ServiceName</span></span>
<span data-ttu-id="84e38-130">Указывает имя службы Microsoft Azure, на которой размещена виртуальная машина.</span><span class="sxs-lookup"><span data-stu-id="84e38-130">Specifies the name of the Microsoft Azure service that hosts the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="84e38-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="84e38-131">CommonParameters</span></span>
<span data-ttu-id="84e38-132">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="84e38-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="84e38-133">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="84e38-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="84e38-134">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="84e38-134">INPUTS</span></span>

## <span data-ttu-id="84e38-135">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="84e38-135">OUTPUTS</span></span>

## <span data-ttu-id="84e38-136">Пуск</span><span class="sxs-lookup"><span data-stu-id="84e38-136">NOTES</span></span>

## <span data-ttu-id="84e38-137">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="84e38-137">RELATED LINKS</span></span>

[<span data-ttu-id="84e38-138">New-AzureVM</span><span class="sxs-lookup"><span data-stu-id="84e38-138">New-AzureVM</span></span>](./New-AzureVM.md)

[<span data-ttu-id="84e38-139">New-AzureQuickVM</span><span class="sxs-lookup"><span data-stu-id="84e38-139">New-AzureQuickVM</span></span>](./New-AzureQuickVM.md)


