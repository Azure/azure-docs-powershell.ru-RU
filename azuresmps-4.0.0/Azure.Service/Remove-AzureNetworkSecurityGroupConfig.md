---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 6AB4700D-571B-497A-9742-2654844553B6
online version: ''
schema: 2.0.0
ms.openlocfilehash: b46f15053639ec295d958766dac846d4f95e0368
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94076151"
---
# <span data-ttu-id="55b31-101">Remove-AzureNetworkSecurityGroupConfig</span><span class="sxs-lookup"><span data-stu-id="55b31-101">Remove-AzureNetworkSecurityGroupConfig</span></span>

## <span data-ttu-id="55b31-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="55b31-102">SYNOPSIS</span></span>

## <span data-ttu-id="55b31-103">Максимальное</span><span class="sxs-lookup"><span data-stu-id="55b31-103">SYNTAX</span></span>

```
Remove-AzureNetworkSecurityGroupConfig [[-NetworkSecurityGroupName] <String>] -VM <IPersistentVM>
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

## <span data-ttu-id="55b31-104">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="55b31-104">DESCRIPTION</span></span>

## <span data-ttu-id="55b31-105">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="55b31-105">EXAMPLES</span></span>

### <span data-ttu-id="55b31-106">1:</span><span class="sxs-lookup"><span data-stu-id="55b31-106">1:</span></span>
```
PS C:\>
```

## <span data-ttu-id="55b31-107">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="55b31-107">PARAMETERS</span></span>

### <span data-ttu-id="55b31-108">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="55b31-108">-InformationAction</span></span>
<span data-ttu-id="55b31-109">Указывает, как этот командлет отвечает на информационное событие.</span><span class="sxs-lookup"><span data-stu-id="55b31-109">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="55b31-110">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="55b31-110">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="55b31-111">Продолжал</span><span class="sxs-lookup"><span data-stu-id="55b31-111">Continue</span></span>
- <span data-ttu-id="55b31-112">Игнорируйте</span><span class="sxs-lookup"><span data-stu-id="55b31-112">Ignore</span></span>
- <span data-ttu-id="55b31-113">INQUIRE</span><span class="sxs-lookup"><span data-stu-id="55b31-113">Inquire</span></span>
- <span data-ttu-id="55b31-114">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="55b31-114">SilentlyContinue</span></span>
- <span data-ttu-id="55b31-115">Остановить</span><span class="sxs-lookup"><span data-stu-id="55b31-115">Stop</span></span>
- <span data-ttu-id="55b31-116">Рвать</span><span class="sxs-lookup"><span data-stu-id="55b31-116">Suspend</span></span>

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

### <span data-ttu-id="55b31-117">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="55b31-117">-InformationVariable</span></span>
<span data-ttu-id="55b31-118">Указывает переменную данных.</span><span class="sxs-lookup"><span data-stu-id="55b31-118">Specifies an information variable.</span></span>

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

### <span data-ttu-id="55b31-119">-NetworkSecurityGroupName</span><span class="sxs-lookup"><span data-stu-id="55b31-119">-NetworkSecurityGroupName</span></span>
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

### <span data-ttu-id="55b31-120">-Profile</span><span class="sxs-lookup"><span data-stu-id="55b31-120">-Profile</span></span>
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

### <span data-ttu-id="55b31-121">-VM</span><span class="sxs-lookup"><span data-stu-id="55b31-121">-VM</span></span>
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

### <span data-ttu-id="55b31-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="55b31-122">CommonParameters</span></span>
<span data-ttu-id="55b31-123">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="55b31-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="55b31-124">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="55b31-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="55b31-125">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="55b31-125">INPUTS</span></span>

## <span data-ttu-id="55b31-126">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="55b31-126">OUTPUTS</span></span>

## <span data-ttu-id="55b31-127">Пуск</span><span class="sxs-lookup"><span data-stu-id="55b31-127">NOTES</span></span>

## <span data-ttu-id="55b31-128">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="55b31-128">RELATED LINKS</span></span>

[<span data-ttu-id="55b31-129">Set-AzureNetworkSecurityGroupConfig</span><span class="sxs-lookup"><span data-stu-id="55b31-129">Set-AzureNetworkSecurityGroupConfig</span></span>](./Set-AzureNetworkSecurityGroupConfig.md)


