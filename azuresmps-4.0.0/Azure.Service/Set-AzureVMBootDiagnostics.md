---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 846B9EB8-8EC2-4BDA-90EF-59098696F460
online version: ''
schema: 2.0.0
ms.openlocfilehash: 0c4e1dedb02286ceaab182e0912198c23ec03ee5
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94075793"
---
# <span data-ttu-id="29e70-101">Set-AzureVMBootDiagnostics</span><span class="sxs-lookup"><span data-stu-id="29e70-101">Set-AzureVMBootDiagnostics</span></span>

## <span data-ttu-id="29e70-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="29e70-102">SYNOPSIS</span></span>

## <span data-ttu-id="29e70-103">Максимальное</span><span class="sxs-lookup"><span data-stu-id="29e70-103">SYNTAX</span></span>

### <span data-ttu-id="29e70-104">EnableBootDiagnostics</span><span class="sxs-lookup"><span data-stu-id="29e70-104">EnableBootDiagnostics</span></span>
```
Set-AzureVMBootDiagnostics [-Enable] -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="29e70-105">DisableBootDiagnostics</span><span class="sxs-lookup"><span data-stu-id="29e70-105">DisableBootDiagnostics</span></span>
```
Set-AzureVMBootDiagnostics [-Disable] -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="29e70-106">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="29e70-106">DESCRIPTION</span></span>

## <span data-ttu-id="29e70-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="29e70-107">EXAMPLES</span></span>

### <span data-ttu-id="29e70-108">1:</span><span class="sxs-lookup"><span data-stu-id="29e70-108">1:</span></span>
```
PS C:\>
```

## <span data-ttu-id="29e70-109">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="29e70-109">PARAMETERS</span></span>

### <span data-ttu-id="29e70-110">-Отключение</span><span class="sxs-lookup"><span data-stu-id="29e70-110">-Disable</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: DisableBootDiagnostics
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="29e70-111">-Enable (включить)</span><span class="sxs-lookup"><span data-stu-id="29e70-111">-Enable</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: EnableBootDiagnostics
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="29e70-112">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="29e70-112">-InformationAction</span></span>
<span data-ttu-id="29e70-113">Указывает, как этот командлет отвечает на информационное событие.</span><span class="sxs-lookup"><span data-stu-id="29e70-113">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="29e70-114">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="29e70-114">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="29e70-115">Продолжал</span><span class="sxs-lookup"><span data-stu-id="29e70-115">Continue</span></span>
- <span data-ttu-id="29e70-116">Игнорируйте</span><span class="sxs-lookup"><span data-stu-id="29e70-116">Ignore</span></span>
- <span data-ttu-id="29e70-117">INQUIRE</span><span class="sxs-lookup"><span data-stu-id="29e70-117">Inquire</span></span>
- <span data-ttu-id="29e70-118">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="29e70-118">SilentlyContinue</span></span>
- <span data-ttu-id="29e70-119">Остановить</span><span class="sxs-lookup"><span data-stu-id="29e70-119">Stop</span></span>
- <span data-ttu-id="29e70-120">Рвать</span><span class="sxs-lookup"><span data-stu-id="29e70-120">Suspend</span></span>

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

### <span data-ttu-id="29e70-121">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="29e70-121">-InformationVariable</span></span>
<span data-ttu-id="29e70-122">Указывает переменную данных.</span><span class="sxs-lookup"><span data-stu-id="29e70-122">Specifies an information variable.</span></span>

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

### <span data-ttu-id="29e70-123">-Profile</span><span class="sxs-lookup"><span data-stu-id="29e70-123">-Profile</span></span>
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

### <span data-ttu-id="29e70-124">-VM</span><span class="sxs-lookup"><span data-stu-id="29e70-124">-VM</span></span>
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

### <span data-ttu-id="29e70-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="29e70-125">CommonParameters</span></span>
<span data-ttu-id="29e70-126">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="29e70-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="29e70-127">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="29e70-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="29e70-128">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="29e70-128">INPUTS</span></span>

## <span data-ttu-id="29e70-129">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="29e70-129">OUTPUTS</span></span>

## <span data-ttu-id="29e70-130">Пуск</span><span class="sxs-lookup"><span data-stu-id="29e70-130">NOTES</span></span>

## <span data-ttu-id="29e70-131">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="29e70-131">RELATED LINKS</span></span>

