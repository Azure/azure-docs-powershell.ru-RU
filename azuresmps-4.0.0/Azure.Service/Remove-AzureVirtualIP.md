---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: B107D789-8F66-4D7D-B126-08ACB0364826
online version: ''
schema: 2.0.0
ms.openlocfilehash: e59df078539e9ea94073defd4c8ea13a69cc2e5f
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94075487"
---
# <span data-ttu-id="72ccb-101">Remove-AzureVirtualIP</span><span class="sxs-lookup"><span data-stu-id="72ccb-101">Remove-AzureVirtualIP</span></span>

## <span data-ttu-id="72ccb-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="72ccb-102">SYNOPSIS</span></span>
<span data-ttu-id="72ccb-103">Удаление виртуального IP-адреса из облачной службы.</span><span class="sxs-lookup"><span data-stu-id="72ccb-103">Deletes a virtual IP address from your Cloud Service.</span></span>

## <span data-ttu-id="72ccb-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="72ccb-104">SYNTAX</span></span>

```
Remove-AzureVirtualIP [-ServiceName] <String> [-VirtualIPName] <String> [-Force] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="72ccb-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="72ccb-105">DESCRIPTION</span></span>
<span data-ttu-id="72ccb-106">Командлет **Remove-AzureVirtualIP** удаляет виртуальный IP-адрес (VIP) из службы Azure.</span><span class="sxs-lookup"><span data-stu-id="72ccb-106">The **Remove-AzureVirtualIP** cmdlet deletes a virtual IP (VIP) from an Azure service.</span></span>
<span data-ttu-id="72ccb-107">Операция выполняется успешно только в том случае, если с виртуальным IP-адресом не связаны конечные точки.</span><span class="sxs-lookup"><span data-stu-id="72ccb-107">The operation succeeds only if the virtual IP has no endpoints associated with it.</span></span>

## <span data-ttu-id="72ccb-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="72ccb-108">EXAMPLES</span></span>

### <span data-ttu-id="72ccb-109">Пример 1: Удаление виртуального IP-адреса из службы</span><span class="sxs-lookup"><span data-stu-id="72ccb-109">Example 1: Remove a virtual IP address from a service</span></span>
```
PS C:\> Remove-AzureVirtualIP -VirtualIPName "Vip01" -ServiceName "ContosoService03"
```

<span data-ttu-id="72ccb-110">Эта команда удаляет виртуальный IP-адрес из службы.</span><span class="sxs-lookup"><span data-stu-id="72ccb-110">This command removes a virtual IP address from a service.</span></span>

## <span data-ttu-id="72ccb-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="72ccb-111">PARAMETERS</span></span>

### <span data-ttu-id="72ccb-112">-Force</span><span class="sxs-lookup"><span data-stu-id="72ccb-112">-Force</span></span>
<span data-ttu-id="72ccb-113">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="72ccb-113">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="72ccb-114">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="72ccb-114">-InformationAction</span></span>
<span data-ttu-id="72ccb-115">Указывает, как этот командлет отвечает на информационное событие.</span><span class="sxs-lookup"><span data-stu-id="72ccb-115">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="72ccb-116">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="72ccb-116">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="72ccb-117">Продолжал</span><span class="sxs-lookup"><span data-stu-id="72ccb-117">Continue</span></span>
- <span data-ttu-id="72ccb-118">Игнорируйте</span><span class="sxs-lookup"><span data-stu-id="72ccb-118">Ignore</span></span>
- <span data-ttu-id="72ccb-119">INQUIRE</span><span class="sxs-lookup"><span data-stu-id="72ccb-119">Inquire</span></span>
- <span data-ttu-id="72ccb-120">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="72ccb-120">SilentlyContinue</span></span>
- <span data-ttu-id="72ccb-121">Остановить</span><span class="sxs-lookup"><span data-stu-id="72ccb-121">Stop</span></span>
- <span data-ttu-id="72ccb-122">Рвать</span><span class="sxs-lookup"><span data-stu-id="72ccb-122">Suspend</span></span>

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

### <span data-ttu-id="72ccb-123">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="72ccb-123">-InformationVariable</span></span>
<span data-ttu-id="72ccb-124">Указывает переменную данных.</span><span class="sxs-lookup"><span data-stu-id="72ccb-124">Specifies an information variable.</span></span>

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

### <span data-ttu-id="72ccb-125">-Profile</span><span class="sxs-lookup"><span data-stu-id="72ccb-125">-Profile</span></span>
<span data-ttu-id="72ccb-126">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="72ccb-126">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="72ccb-127">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="72ccb-127">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="72ccb-128">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="72ccb-128">-ServiceName</span></span>
<span data-ttu-id="72ccb-129">Указывает имя службы, из которой нужно удалить виртуальный IP-адрес.</span><span class="sxs-lookup"><span data-stu-id="72ccb-129">Specifies the name of the service from which to remove a virtual IP address.</span></span>

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

### <span data-ttu-id="72ccb-130">-VirtualIPName</span><span class="sxs-lookup"><span data-stu-id="72ccb-130">-VirtualIPName</span></span>
<span data-ttu-id="72ccb-131">Указывает имя виртуального IP-адреса, который нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="72ccb-131">Specifies the name of the virtual IP address to remove.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="72ccb-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="72ccb-132">CommonParameters</span></span>
<span data-ttu-id="72ccb-133">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="72ccb-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="72ccb-134">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="72ccb-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="72ccb-135">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="72ccb-135">INPUTS</span></span>

## <span data-ttu-id="72ccb-136">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="72ccb-136">OUTPUTS</span></span>

### <span data-ttu-id="72ccb-137">Microsoft. WindowsAzure. Commands. Utilities. Common. ManagementOperationContext</span><span class="sxs-lookup"><span data-stu-id="72ccb-137">Microsoft.WindowsAzure.Commands.Utilities.Common.ManagementOperationContext</span></span>

## <span data-ttu-id="72ccb-138">Пуск</span><span class="sxs-lookup"><span data-stu-id="72ccb-138">NOTES</span></span>

## <span data-ttu-id="72ccb-139">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="72ccb-139">RELATED LINKS</span></span>

[<span data-ttu-id="72ccb-140">Add-AzureVirtualIP</span><span class="sxs-lookup"><span data-stu-id="72ccb-140">Add-AzureVirtualIP</span></span>](./Add-AzureVirtualIP.md)


