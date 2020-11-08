---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: FE31EE5C-830F-4B5E-82DB-C881032EF05C
online version: ''
schema: 2.0.0
ms.openlocfilehash: 9c1160478da2c84f2d792ab570b05d544f4537bc
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94076394"
---
# <span data-ttu-id="2bfa1-101">Add-AzureNetworkInterfaceConfig</span><span class="sxs-lookup"><span data-stu-id="2bfa1-101">Add-AzureNetworkInterfaceConfig</span></span>

## <span data-ttu-id="2bfa1-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="2bfa1-102">SYNOPSIS</span></span>

## <span data-ttu-id="2bfa1-103">Максимальное</span><span class="sxs-lookup"><span data-stu-id="2bfa1-103">SYNTAX</span></span>

```
Add-AzureNetworkInterfaceConfig [-Name] <String> [-SubnetName] <String> [[-StaticVNetIPAddress] <String>]
 [[-NetworkSecurityGroup] <String>] [[-IPForwarding] <String>] -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="2bfa1-104">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="2bfa1-104">DESCRIPTION</span></span>

## <span data-ttu-id="2bfa1-105">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="2bfa1-105">EXAMPLES</span></span>

### <span data-ttu-id="2bfa1-106">1:</span><span class="sxs-lookup"><span data-stu-id="2bfa1-106">1:</span></span>
```
PS C:\>
```

## <span data-ttu-id="2bfa1-107">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="2bfa1-107">PARAMETERS</span></span>

### <span data-ttu-id="2bfa1-108">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="2bfa1-108">-InformationAction</span></span>
<span data-ttu-id="2bfa1-109">Указывает, как этот командлет отвечает на информационное событие.</span><span class="sxs-lookup"><span data-stu-id="2bfa1-109">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="2bfa1-110">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="2bfa1-110">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="2bfa1-111">Продолжал</span><span class="sxs-lookup"><span data-stu-id="2bfa1-111">Continue</span></span>
- <span data-ttu-id="2bfa1-112">Игнорируйте</span><span class="sxs-lookup"><span data-stu-id="2bfa1-112">Ignore</span></span>
- <span data-ttu-id="2bfa1-113">INQUIRE</span><span class="sxs-lookup"><span data-stu-id="2bfa1-113">Inquire</span></span>
- <span data-ttu-id="2bfa1-114">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="2bfa1-114">SilentlyContinue</span></span>
- <span data-ttu-id="2bfa1-115">Остановить</span><span class="sxs-lookup"><span data-stu-id="2bfa1-115">Stop</span></span>
- <span data-ttu-id="2bfa1-116">Рвать</span><span class="sxs-lookup"><span data-stu-id="2bfa1-116">Suspend</span></span>

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

### <span data-ttu-id="2bfa1-117">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="2bfa1-117">-InformationVariable</span></span>
<span data-ttu-id="2bfa1-118">Указывает переменную данных.</span><span class="sxs-lookup"><span data-stu-id="2bfa1-118">Specifies an information variable.</span></span>

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

### <span data-ttu-id="2bfa1-119">-IPForwarding</span><span class="sxs-lookup"><span data-stu-id="2bfa1-119">-IPForwarding</span></span>
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

### <span data-ttu-id="2bfa1-120">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="2bfa1-120">-Name</span></span>
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

### <span data-ttu-id="2bfa1-121">-NetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="2bfa1-121">-NetworkSecurityGroup</span></span>
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

### <span data-ttu-id="2bfa1-122">-Profile</span><span class="sxs-lookup"><span data-stu-id="2bfa1-122">-Profile</span></span>
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

### <span data-ttu-id="2bfa1-123">-StaticVNetIPAddress</span><span class="sxs-lookup"><span data-stu-id="2bfa1-123">-StaticVNetIPAddress</span></span>
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

### <span data-ttu-id="2bfa1-124">-SubnetName</span><span class="sxs-lookup"><span data-stu-id="2bfa1-124">-SubnetName</span></span>
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

### <span data-ttu-id="2bfa1-125">-VM</span><span class="sxs-lookup"><span data-stu-id="2bfa1-125">-VM</span></span>
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

### <span data-ttu-id="2bfa1-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2bfa1-126">CommonParameters</span></span>
<span data-ttu-id="2bfa1-127">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="2bfa1-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2bfa1-128">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2bfa1-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2bfa1-129">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="2bfa1-129">INPUTS</span></span>

## <span data-ttu-id="2bfa1-130">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="2bfa1-130">OUTPUTS</span></span>

## <span data-ttu-id="2bfa1-131">Пуск</span><span class="sxs-lookup"><span data-stu-id="2bfa1-131">NOTES</span></span>

## <span data-ttu-id="2bfa1-132">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="2bfa1-132">RELATED LINKS</span></span>

[<span data-ttu-id="2bfa1-133">Get-AzureNetworkInterfaceConfig</span><span class="sxs-lookup"><span data-stu-id="2bfa1-133">Get-AzureNetworkInterfaceConfig</span></span>](./Get-AzureNetworkInterfaceConfig.md)

[<span data-ttu-id="2bfa1-134">Remove-AzureNetworkInterfaceConfig</span><span class="sxs-lookup"><span data-stu-id="2bfa1-134">Remove-AzureNetworkInterfaceConfig</span></span>](./Remove-AzureNetworkInterfaceConfig.md)

[<span data-ttu-id="2bfa1-135">Set-AzureNetworkInterfaceConfig</span><span class="sxs-lookup"><span data-stu-id="2bfa1-135">Set-AzureNetworkInterfaceConfig</span></span>](./Set-AzureNetworkInterfaceConfig.md)


