---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: A4E88106-1B47-4ACD-8F35-027D16EA7791
online version: ''
schema: 2.0.0
ms.openlocfilehash: 85b3422581fa884245807f258adcc31d52404c53
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94075805"
---
# <span data-ttu-id="3d15d-101">Set-AzureNetworkInterfaceConfig</span><span class="sxs-lookup"><span data-stu-id="3d15d-101">Set-AzureNetworkInterfaceConfig</span></span>

## <span data-ttu-id="3d15d-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="3d15d-102">SYNOPSIS</span></span>

## <span data-ttu-id="3d15d-103">Максимальное</span><span class="sxs-lookup"><span data-stu-id="3d15d-103">SYNTAX</span></span>

```
Set-AzureNetworkInterfaceConfig [-Name] <String> [-SubnetName] <String> [[-StaticVNetIPAddress] <String>]
 [[-NetworkSecurityGroup] <String>] [[-IPForwarding] <String>] -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="3d15d-104">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="3d15d-104">DESCRIPTION</span></span>

## <span data-ttu-id="3d15d-105">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="3d15d-105">EXAMPLES</span></span>

### <span data-ttu-id="3d15d-106">1:</span><span class="sxs-lookup"><span data-stu-id="3d15d-106">1:</span></span>
```
PS C:\>
```

## <span data-ttu-id="3d15d-107">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="3d15d-107">PARAMETERS</span></span>

### <span data-ttu-id="3d15d-108">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="3d15d-108">-InformationAction</span></span>
<span data-ttu-id="3d15d-109">Указывает, как этот командлет отвечает на информационное событие.</span><span class="sxs-lookup"><span data-stu-id="3d15d-109">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="3d15d-110">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="3d15d-110">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="3d15d-111">Продолжал</span><span class="sxs-lookup"><span data-stu-id="3d15d-111">Continue</span></span>
- <span data-ttu-id="3d15d-112">Игнорируйте</span><span class="sxs-lookup"><span data-stu-id="3d15d-112">Ignore</span></span>
- <span data-ttu-id="3d15d-113">INQUIRE</span><span class="sxs-lookup"><span data-stu-id="3d15d-113">Inquire</span></span>
- <span data-ttu-id="3d15d-114">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="3d15d-114">SilentlyContinue</span></span>
- <span data-ttu-id="3d15d-115">Остановить</span><span class="sxs-lookup"><span data-stu-id="3d15d-115">Stop</span></span>
- <span data-ttu-id="3d15d-116">Рвать</span><span class="sxs-lookup"><span data-stu-id="3d15d-116">Suspend</span></span>

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

### <span data-ttu-id="3d15d-117">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="3d15d-117">-InformationVariable</span></span>
<span data-ttu-id="3d15d-118">Указывает переменную данных.</span><span class="sxs-lookup"><span data-stu-id="3d15d-118">Specifies an information variable.</span></span>

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

### <span data-ttu-id="3d15d-119">-IPForwarding</span><span class="sxs-lookup"><span data-stu-id="3d15d-119">-IPForwarding</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3d15d-120">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="3d15d-120">-Name</span></span>
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

### <span data-ttu-id="3d15d-121">-NetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="3d15d-121">-NetworkSecurityGroup</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3d15d-122">-Profile</span><span class="sxs-lookup"><span data-stu-id="3d15d-122">-Profile</span></span>
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

### <span data-ttu-id="3d15d-123">-StaticVNetIPAddress</span><span class="sxs-lookup"><span data-stu-id="3d15d-123">-StaticVNetIPAddress</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3d15d-124">-SubnetName</span><span class="sxs-lookup"><span data-stu-id="3d15d-124">-SubnetName</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3d15d-125">-VM</span><span class="sxs-lookup"><span data-stu-id="3d15d-125">-VM</span></span>
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

### <span data-ttu-id="3d15d-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3d15d-126">CommonParameters</span></span>
<span data-ttu-id="3d15d-127">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="3d15d-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3d15d-128">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3d15d-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3d15d-129">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="3d15d-129">INPUTS</span></span>

## <span data-ttu-id="3d15d-130">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="3d15d-130">OUTPUTS</span></span>

## <span data-ttu-id="3d15d-131">Пуск</span><span class="sxs-lookup"><span data-stu-id="3d15d-131">NOTES</span></span>

## <span data-ttu-id="3d15d-132">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="3d15d-132">RELATED LINKS</span></span>

[<span data-ttu-id="3d15d-133">Add-AzureNetworkInterfaceConfig</span><span class="sxs-lookup"><span data-stu-id="3d15d-133">Add-AzureNetworkInterfaceConfig</span></span>](./Add-AzureNetworkInterfaceConfig.md)

[<span data-ttu-id="3d15d-134">Get-AzureNetworkInterfaceConfig</span><span class="sxs-lookup"><span data-stu-id="3d15d-134">Get-AzureNetworkInterfaceConfig</span></span>](./Get-AzureNetworkInterfaceConfig.md)

[<span data-ttu-id="3d15d-135">Remove-AzureNetworkInterfaceConfig</span><span class="sxs-lookup"><span data-stu-id="3d15d-135">Remove-AzureNetworkInterfaceConfig</span></span>](./Remove-AzureNetworkInterfaceConfig.md)


