---
external help file: Microsoft.WindowsAzure.Commands.TrafficManager.dll-Help.xml
ms.assetid: ECE9C2A6-7DA2-4477-B877-9970FBE26D7C
online version: ''
schema: 2.0.0
ms.openlocfilehash: 8f378cbf8926a650699ec50a2a0a42873dcb7528
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94075693"
---
# <span data-ttu-id="77771-101">Disable-AzureTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="77771-101">Disable-AzureTrafficManagerProfile</span></span>

## <span data-ttu-id="77771-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="77771-102">SYNOPSIS</span></span>
<span data-ttu-id="77771-103">Отключение профиля диспетчера трафика.</span><span class="sxs-lookup"><span data-stu-id="77771-103">Disables a Traffic Manager profile.</span></span>

## <span data-ttu-id="77771-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="77771-104">SYNTAX</span></span>

```
Disable-AzureTrafficManagerProfile -Name <String> [-PassThru] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="77771-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="77771-105">DESCRIPTION</span></span>
<span data-ttu-id="77771-106">Командлет **Disable-AzureTrafficManagerProfile** отключает профиль диспетчера трафика Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="77771-106">The **Disable-AzureTrafficManagerProfile** cmdlet disables a Microsoft Azure Traffic Manager profile.</span></span>
<span data-ttu-id="77771-107">Вы можете использовать параметр *PassThru* , чтобы показать, выполняется ли операция успешно.</span><span class="sxs-lookup"><span data-stu-id="77771-107">You can use the *PassThru* parameter to display whether the operation succeeds.</span></span>

## <span data-ttu-id="77771-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="77771-108">EXAMPLES</span></span>

### <span data-ttu-id="77771-109">Пример 1: отключение профиля диспетчера трафика и отображение результатов</span><span class="sxs-lookup"><span data-stu-id="77771-109">Example 1: Disable a Traffic Manager profile and display the results</span></span>
```
PS C:\>Disable-AzureTrafficManagerProfile -Name "MyProfile" -PassThru
True
```

<span data-ttu-id="77771-110">Эта команда отключает профиль диспетчера трафика с именем отобразите.</span><span class="sxs-lookup"><span data-stu-id="77771-110">This command disables the Traffic Manager profile named MyProfile.</span></span>
<span data-ttu-id="77771-111">Команда определяет параметр *PassThru* , чтобы показать, успешно ли команда выполнена.</span><span class="sxs-lookup"><span data-stu-id="77771-111">The command specifies the *PassThru* parameter to display whether the command succeeded.</span></span>

### <span data-ttu-id="77771-112">Пример 2: отключение профиля диспетчера трафика и отображение результатов</span><span class="sxs-lookup"><span data-stu-id="77771-112">Example 2: Disable a Traffic Manager profile and display no results</span></span>
```
PS C:\>Disable-AzureTrafficManagerProfile -Name "MyProfile"
```

<span data-ttu-id="77771-113">Эта команда отключает профиль диспетчера трафика с именем отобразите, но не показывает, была ли команда выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="77771-113">This command disables the Traffic Manager profile named MyProfile but does not display whether the command succeeded.</span></span>

## <span data-ttu-id="77771-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="77771-114">PARAMETERS</span></span>

### <span data-ttu-id="77771-115">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="77771-115">-Name</span></span>
<span data-ttu-id="77771-116">Указывает имя профиля диспетчера трафика, который нужно отключить.</span><span class="sxs-lookup"><span data-stu-id="77771-116">Specifies the name of the Traffic Manager profile to disable.</span></span>

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

### <span data-ttu-id="77771-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="77771-117">-PassThru</span></span>
<span data-ttu-id="77771-118">Возвращает $True, если операция выполнена успешно. в противном случае $False.</span><span class="sxs-lookup"><span data-stu-id="77771-118">Returns $True if the operation succeeded; otherwise, $False.</span></span>
<span data-ttu-id="77771-119">По умолчанию этот командлет не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="77771-119">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="77771-120">-Profile</span><span class="sxs-lookup"><span data-stu-id="77771-120">-Profile</span></span>
<span data-ttu-id="77771-121">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="77771-121">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="77771-122">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="77771-122">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="77771-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="77771-123">CommonParameters</span></span>
<span data-ttu-id="77771-124">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="77771-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="77771-125">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="77771-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="77771-126">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="77771-126">INPUTS</span></span>

## <span data-ttu-id="77771-127">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="77771-127">OUTPUTS</span></span>

### <span data-ttu-id="77771-128">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="77771-128">System.Boolean</span></span>
<span data-ttu-id="77771-129">Этот командлет создает $True или $False.</span><span class="sxs-lookup"><span data-stu-id="77771-129">This cmdlet generates $True or $False.</span></span>
<span data-ttu-id="77771-130">Если операция выполнена успешно и вы указываете параметр *PassThru* , этот командлет возвращает значение $true.</span><span class="sxs-lookup"><span data-stu-id="77771-130">If the operation is successful and if you specify the *PassThru* parameter, this cmdlet returns a value of $True.</span></span>

## <span data-ttu-id="77771-131">Пуск</span><span class="sxs-lookup"><span data-stu-id="77771-131">NOTES</span></span>

## <span data-ttu-id="77771-132">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="77771-132">RELATED LINKS</span></span>

[<span data-ttu-id="77771-133">Enable-AzureTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="77771-133">Enable-AzureTrafficManagerProfile</span></span>](./Enable-AzureTrafficManagerProfile.md)

[<span data-ttu-id="77771-134">Get-AzureTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="77771-134">Get-AzureTrafficManagerProfile</span></span>](./Get-AzureTrafficManagerProfile.md)

[<span data-ttu-id="77771-135">New-AzureTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="77771-135">New-AzureTrafficManagerProfile</span></span>](./New-AzureTrafficManagerProfile.md)

[<span data-ttu-id="77771-136">Remove-AzureTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="77771-136">Remove-AzureTrafficManagerProfile</span></span>](./Remove-AzureTrafficManagerProfile.md)

[<span data-ttu-id="77771-137">Set-AzureTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="77771-137">Set-AzureTrafficManagerProfile</span></span>](./Set-AzureTrafficManagerProfile.md)


