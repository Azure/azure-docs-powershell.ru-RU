---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 58329D8A-CB54-46FB-84A7-C31F00C13827
online version: ''
schema: 2.0.0
ms.openlocfilehash: 6333430682de7693b6b87f9d037dea66725bfed8
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94076132"
---
# <span data-ttu-id="84b8b-101">Remove-AzureRouteTable</span><span class="sxs-lookup"><span data-stu-id="84b8b-101">Remove-AzureRouteTable</span></span>

## <span data-ttu-id="84b8b-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="84b8b-102">SYNOPSIS</span></span>
<span data-ttu-id="84b8b-103">Удаляет таблицу маршрутов.</span><span class="sxs-lookup"><span data-stu-id="84b8b-103">Removes a route table.</span></span>

## <span data-ttu-id="84b8b-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="84b8b-104">SYNTAX</span></span>

```
Remove-AzureRouteTable -Name <String> [-PassThru] [-Force] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="84b8b-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="84b8b-105">DESCRIPTION</span></span>
<span data-ttu-id="84b8b-106">Командлет **Remove-AzureRouteTable** удаляет таблицу маршрутов из подписки.</span><span class="sxs-lookup"><span data-stu-id="84b8b-106">The **Remove-AzureRouteTable** cmdlet removes a route table from your subscription.</span></span>
<span data-ttu-id="84b8b-107">Если таблица маршрутов связана с подсетью, удалить ее нельзя.</span><span class="sxs-lookup"><span data-stu-id="84b8b-107">If a route table is associated to a subnet, you cannot remove the table.</span></span>

## <span data-ttu-id="84b8b-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="84b8b-108">EXAMPLES</span></span>

### <span data-ttu-id="84b8b-109">Пример 1: удаление таблицы маршрутов</span><span class="sxs-lookup"><span data-stu-id="84b8b-109">Example 1: Remove a route table</span></span>
```
PS C:\> Remove-AzureRouteTable -Name "PublicRouteTable"
```

<span data-ttu-id="84b8b-110">Эта команда удаляет таблицу маршрутов с именем PublicRouteTable.</span><span class="sxs-lookup"><span data-stu-id="84b8b-110">This command removes the route table named PublicRouteTable.</span></span>

## <span data-ttu-id="84b8b-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="84b8b-111">PARAMETERS</span></span>

### <span data-ttu-id="84b8b-112">-Force</span><span class="sxs-lookup"><span data-stu-id="84b8b-112">-Force</span></span>
<span data-ttu-id="84b8b-113">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="84b8b-113">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="84b8b-114">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="84b8b-114">-Name</span></span>
<span data-ttu-id="84b8b-115">Указывает имя таблицы маршрутов, которую удаляет этот командлет.</span><span class="sxs-lookup"><span data-stu-id="84b8b-115">Specifies the name of the route table that this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="84b8b-116">-PassThru</span><span class="sxs-lookup"><span data-stu-id="84b8b-116">-PassThru</span></span>
<span data-ttu-id="84b8b-117">Возвращает объект, который представляет собой элемент, с которым вы работаете.</span><span class="sxs-lookup"><span data-stu-id="84b8b-117">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="84b8b-118">По умолчанию этот командлет не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="84b8b-118">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="84b8b-119">-Profile</span><span class="sxs-lookup"><span data-stu-id="84b8b-119">-Profile</span></span>
<span data-ttu-id="84b8b-120">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="84b8b-120">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="84b8b-121">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="84b8b-121">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="84b8b-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="84b8b-122">CommonParameters</span></span>
<span data-ttu-id="84b8b-123">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="84b8b-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="84b8b-124">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="84b8b-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="84b8b-125">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="84b8b-125">INPUTS</span></span>

## <span data-ttu-id="84b8b-126">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="84b8b-126">OUTPUTS</span></span>

## <span data-ttu-id="84b8b-127">Пуск</span><span class="sxs-lookup"><span data-stu-id="84b8b-127">NOTES</span></span>

## <span data-ttu-id="84b8b-128">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="84b8b-128">RELATED LINKS</span></span>

[<span data-ttu-id="84b8b-129">Get-AzureRouteTable</span><span class="sxs-lookup"><span data-stu-id="84b8b-129">Get-AzureRouteTable</span></span>](./Get-AzureRouteTable.md)

[<span data-ttu-id="84b8b-130">New-AzureRouteTable</span><span class="sxs-lookup"><span data-stu-id="84b8b-130">New-AzureRouteTable</span></span>](./New-AzureRouteTable.md)
