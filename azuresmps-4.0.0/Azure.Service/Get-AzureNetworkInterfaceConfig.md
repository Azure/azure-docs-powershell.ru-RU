---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: EE96AC92-02A8-4A40-A26D-0882673E51A5
online version: ''
schema: 2.0.0
ms.openlocfilehash: 2dca85290564217f5c4c319ef3531d4c31500fcd
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94076584"
---
# <span data-ttu-id="88bc4-101">Get-AzureNetworkInterfaceConfig</span><span class="sxs-lookup"><span data-stu-id="88bc4-101">Get-AzureNetworkInterfaceConfig</span></span>

## <span data-ttu-id="88bc4-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="88bc4-102">SYNOPSIS</span></span>

## <span data-ttu-id="88bc4-103">Максимальное</span><span class="sxs-lookup"><span data-stu-id="88bc4-103">SYNTAX</span></span>

```
Get-AzureNetworkInterfaceConfig [[-Name] <String>] -VM <PersistentVMRoleContext>
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="88bc4-104">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="88bc4-104">DESCRIPTION</span></span>

## <span data-ttu-id="88bc4-105">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="88bc4-105">EXAMPLES</span></span>

### <span data-ttu-id="88bc4-106">1:</span><span class="sxs-lookup"><span data-stu-id="88bc4-106">1:</span></span>
```
PS C:\>
```

## <span data-ttu-id="88bc4-107">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="88bc4-107">PARAMETERS</span></span>

### <span data-ttu-id="88bc4-108">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="88bc4-108">-InformationAction</span></span>
<span data-ttu-id="88bc4-109">Указывает, как этот командлет отвечает на информационное событие.</span><span class="sxs-lookup"><span data-stu-id="88bc4-109">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="88bc4-110">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="88bc4-110">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="88bc4-111">Продолжал</span><span class="sxs-lookup"><span data-stu-id="88bc4-111">Continue</span></span>
- <span data-ttu-id="88bc4-112">Игнорируйте</span><span class="sxs-lookup"><span data-stu-id="88bc4-112">Ignore</span></span>
- <span data-ttu-id="88bc4-113">INQUIRE</span><span class="sxs-lookup"><span data-stu-id="88bc4-113">Inquire</span></span>
- <span data-ttu-id="88bc4-114">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="88bc4-114">SilentlyContinue</span></span>
- <span data-ttu-id="88bc4-115">Остановить</span><span class="sxs-lookup"><span data-stu-id="88bc4-115">Stop</span></span>
- <span data-ttu-id="88bc4-116">Рвать</span><span class="sxs-lookup"><span data-stu-id="88bc4-116">Suspend</span></span>

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

### <span data-ttu-id="88bc4-117">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="88bc4-117">-InformationVariable</span></span>
<span data-ttu-id="88bc4-118">Указывает переменную данных.</span><span class="sxs-lookup"><span data-stu-id="88bc4-118">Specifies an information variable.</span></span>

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

### <span data-ttu-id="88bc4-119">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="88bc4-119">-Name</span></span>
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

### <span data-ttu-id="88bc4-120">-VM</span><span class="sxs-lookup"><span data-stu-id="88bc4-120">-VM</span></span>
```yaml
Type: PersistentVMRoleContext
Parameter Sets: (All)
Aliases: InputObject

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="88bc4-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="88bc4-121">CommonParameters</span></span>
<span data-ttu-id="88bc4-122">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="88bc4-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="88bc4-123">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="88bc4-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="88bc4-124">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="88bc4-124">INPUTS</span></span>

## <span data-ttu-id="88bc4-125">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="88bc4-125">OUTPUTS</span></span>

## <span data-ttu-id="88bc4-126">Пуск</span><span class="sxs-lookup"><span data-stu-id="88bc4-126">NOTES</span></span>

## <span data-ttu-id="88bc4-127">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="88bc4-127">RELATED LINKS</span></span>

[<span data-ttu-id="88bc4-128">Add-AzureNetworkInterfaceConfig</span><span class="sxs-lookup"><span data-stu-id="88bc4-128">Add-AzureNetworkInterfaceConfig</span></span>](./Add-AzureNetworkInterfaceConfig.md)

[<span data-ttu-id="88bc4-129">Remove-AzureNetworkInterfaceConfig</span><span class="sxs-lookup"><span data-stu-id="88bc4-129">Remove-AzureNetworkInterfaceConfig</span></span>](./Remove-AzureNetworkInterfaceConfig.md)

[<span data-ttu-id="88bc4-130">Set-AzureNetworkInterfaceConfig</span><span class="sxs-lookup"><span data-stu-id="88bc4-130">Set-AzureNetworkInterfaceConfig</span></span>](./Set-AzureNetworkInterfaceConfig.md)


