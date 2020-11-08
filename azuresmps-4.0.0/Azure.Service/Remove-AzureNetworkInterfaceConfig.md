---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 185C2680-501F-497D-81B2-5F6E30A91F16
online version: ''
schema: 2.0.0
ms.openlocfilehash: 55e9f6f026e7e524613a0e070767bc2ab26f6d66
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94076466"
---
# <span data-ttu-id="4af91-101">Remove-AzureNetworkInterfaceConfig</span><span class="sxs-lookup"><span data-stu-id="4af91-101">Remove-AzureNetworkInterfaceConfig</span></span>

## <span data-ttu-id="4af91-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="4af91-102">SYNOPSIS</span></span>

## <span data-ttu-id="4af91-103">Максимальное</span><span class="sxs-lookup"><span data-stu-id="4af91-103">SYNTAX</span></span>

```
Remove-AzureNetworkInterfaceConfig [-Name] <String> -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="4af91-104">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="4af91-104">DESCRIPTION</span></span>

## <span data-ttu-id="4af91-105">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="4af91-105">EXAMPLES</span></span>

### <span data-ttu-id="4af91-106">1:</span><span class="sxs-lookup"><span data-stu-id="4af91-106">1:</span></span>
```
PS C:\>
```

## <span data-ttu-id="4af91-107">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="4af91-107">PARAMETERS</span></span>

### <span data-ttu-id="4af91-108">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="4af91-108">-InformationAction</span></span>
<span data-ttu-id="4af91-109">Указывает, как этот командлет отвечает на информационное событие.</span><span class="sxs-lookup"><span data-stu-id="4af91-109">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="4af91-110">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="4af91-110">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="4af91-111">Продолжал</span><span class="sxs-lookup"><span data-stu-id="4af91-111">Continue</span></span>
- <span data-ttu-id="4af91-112">Игнорируйте</span><span class="sxs-lookup"><span data-stu-id="4af91-112">Ignore</span></span>
- <span data-ttu-id="4af91-113">INQUIRE</span><span class="sxs-lookup"><span data-stu-id="4af91-113">Inquire</span></span>
- <span data-ttu-id="4af91-114">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="4af91-114">SilentlyContinue</span></span>
- <span data-ttu-id="4af91-115">Остановить</span><span class="sxs-lookup"><span data-stu-id="4af91-115">Stop</span></span>
- <span data-ttu-id="4af91-116">Рвать</span><span class="sxs-lookup"><span data-stu-id="4af91-116">Suspend</span></span>

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

### <span data-ttu-id="4af91-117">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="4af91-117">-InformationVariable</span></span>
<span data-ttu-id="4af91-118">Указывает переменную данных.</span><span class="sxs-lookup"><span data-stu-id="4af91-118">Specifies an information variable.</span></span>

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

### <span data-ttu-id="4af91-119">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="4af91-119">-Name</span></span>
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

### <span data-ttu-id="4af91-120">-Profile</span><span class="sxs-lookup"><span data-stu-id="4af91-120">-Profile</span></span>
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

### <span data-ttu-id="4af91-121">-VM</span><span class="sxs-lookup"><span data-stu-id="4af91-121">-VM</span></span>
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

### <span data-ttu-id="4af91-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4af91-122">CommonParameters</span></span>
<span data-ttu-id="4af91-123">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="4af91-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4af91-124">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4af91-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4af91-125">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="4af91-125">INPUTS</span></span>

## <span data-ttu-id="4af91-126">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="4af91-126">OUTPUTS</span></span>

## <span data-ttu-id="4af91-127">Пуск</span><span class="sxs-lookup"><span data-stu-id="4af91-127">NOTES</span></span>

## <span data-ttu-id="4af91-128">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="4af91-128">RELATED LINKS</span></span>

[<span data-ttu-id="4af91-129">Add-AzureNetworkInterfaceConfig</span><span class="sxs-lookup"><span data-stu-id="4af91-129">Add-AzureNetworkInterfaceConfig</span></span>](./Add-AzureNetworkInterfaceConfig.md)

[<span data-ttu-id="4af91-130">Get-AzureNetworkInterfaceConfig</span><span class="sxs-lookup"><span data-stu-id="4af91-130">Get-AzureNetworkInterfaceConfig</span></span>](./Get-AzureNetworkInterfaceConfig.md)

[<span data-ttu-id="4af91-131">Set-AzureNetworkInterfaceConfig</span><span class="sxs-lookup"><span data-stu-id="4af91-131">Set-AzureNetworkInterfaceConfig</span></span>](./Set-AzureNetworkInterfaceConfig.md)


