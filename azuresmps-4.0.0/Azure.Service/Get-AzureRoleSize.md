---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 2CBF8DEF-954C-4D9F-B495-C2F76550BC79
online version: ''
schema: 2.0.0
ms.openlocfilehash: 35f7e8a7a08ac2793b7e4aeb8615e5fb8fc1f727
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94075615"
---
# <span data-ttu-id="4d29d-101">Get-AzureRoleSize</span><span class="sxs-lookup"><span data-stu-id="4d29d-101">Get-AzureRoleSize</span></span>

## <span data-ttu-id="4d29d-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="4d29d-102">SYNOPSIS</span></span>
<span data-ttu-id="4d29d-103">Возвращает сведения о размере роли для текущей подписки.</span><span class="sxs-lookup"><span data-stu-id="4d29d-103">Gets the role size information for the current subscription.</span></span>

## <span data-ttu-id="4d29d-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="4d29d-104">SYNTAX</span></span>

```
Get-AzureRoleSize [[-InstanceSize] <String>] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="4d29d-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="4d29d-105">DESCRIPTION</span></span>
<span data-ttu-id="4d29d-106">Командлет **Get-AzureRoleSize** получает сведения о размере роли для текущей подписки.</span><span class="sxs-lookup"><span data-stu-id="4d29d-106">The **Get-AzureRoleSize** cmdlet gets the role size information for the current subscription.</span></span>

## <span data-ttu-id="4d29d-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="4d29d-107">EXAMPLES</span></span>

### <span data-ttu-id="4d29d-108">Пример 1: получение сведений о размере роли</span><span class="sxs-lookup"><span data-stu-id="4d29d-108">Example 1: Get role size information</span></span>
```
PS C:\> Get-AzureRoleSize

          InstanceSize               : A6
          RoleSizeLabel              :
          Cores                      : 4
          MemoryInMb                 : 28672
          SupportedByWebWorkerRoles  : True
          SupportedByVirtualMachines : True
          OperationDescription       : Get-AzureRoleSize
          OperationId                : c5ed7b3a-03b3-548d-876b-6688c5b29cce
          OperationStatus            : Succeeded

          InstanceSize               : A7
          RoleSizeLabel              :
          Cores                      : 8
          MemoryInMb                 : 57344
          SupportedByWebWorkerRoles  : True
          SupportedByVirtualMachines : True
          OperationDescription       : Get-AzureRoleSize
          OperationId                : c5ed7b3a-03b3-548d-876b-6688c5b29cce
          OperationStatus            : Succeeded
```

<span data-ttu-id="4d29d-109">Эта команда получает сведения о размере роли для текущей подписки.</span><span class="sxs-lookup"><span data-stu-id="4d29d-109">This command gets role size information for the current subscription.</span></span>

### <span data-ttu-id="4d29d-110">Пример 2: получение сведений о размере роли и указание имени размера роли</span><span class="sxs-lookup"><span data-stu-id="4d29d-110">Example 2: Get role size information and specify the role size name</span></span>
```
PS C:\> Get-AzureRoleSize -InstanceSize A7

          InstanceSize               : A7
          RoleSizeLabel              :
          Cores                      : 8
          MemoryInMb                 : 57344
          SupportedByWebWorkerRoles  : True
          SupportedByVirtualMachines : True
          OperationDescription       : Get-AzureRoleSize
          OperationId                : c5ed7b3a-03b3-548d-876b-6688c5b29cce
          OperationStatus            : Succeeded
```

<span data-ttu-id="4d29d-111">Эта команда получает сведения о размере роли для указанного размера роли.</span><span class="sxs-lookup"><span data-stu-id="4d29d-111">This command gets role size information for the specified role size.</span></span>

### <span data-ttu-id="4d29d-112">Пример 3: получение сведений о размере роли для всех виртуальных машин во всех службах Azure</span><span class="sxs-lookup"><span data-stu-id="4d29d-112">Example 3: Get role size information for all virtual machines in all of the Azure services</span></span>
```
PS C:\> Get-AzureService | Get-AzureVM | Get-AzureRoleSize
```

<span data-ttu-id="4d29d-113">Эта команда получает сведения о размере роли для всех виртуальных машин во всех службах Azure.</span><span class="sxs-lookup"><span data-stu-id="4d29d-113">This command gets role size information for all virtual machines in all of the Azure services.</span></span>

## <span data-ttu-id="4d29d-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="4d29d-114">PARAMETERS</span></span>

### <span data-ttu-id="4d29d-115">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="4d29d-115">-InformationAction</span></span>
<span data-ttu-id="4d29d-116">Указывает, как этот командлет отвечает на информационное событие.</span><span class="sxs-lookup"><span data-stu-id="4d29d-116">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="4d29d-117">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="4d29d-117">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="4d29d-118">Продолжал</span><span class="sxs-lookup"><span data-stu-id="4d29d-118">Continue</span></span>
- <span data-ttu-id="4d29d-119">Игнорируйте</span><span class="sxs-lookup"><span data-stu-id="4d29d-119">Ignore</span></span>
- <span data-ttu-id="4d29d-120">INQUIRE</span><span class="sxs-lookup"><span data-stu-id="4d29d-120">Inquire</span></span>
- <span data-ttu-id="4d29d-121">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="4d29d-121">SilentlyContinue</span></span>
- <span data-ttu-id="4d29d-122">Остановить</span><span class="sxs-lookup"><span data-stu-id="4d29d-122">Stop</span></span>
- <span data-ttu-id="4d29d-123">Рвать</span><span class="sxs-lookup"><span data-stu-id="4d29d-123">Suspend</span></span>

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

### <span data-ttu-id="4d29d-124">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="4d29d-124">-InformationVariable</span></span>
<span data-ttu-id="4d29d-125">Указывает переменную данных.</span><span class="sxs-lookup"><span data-stu-id="4d29d-125">Specifies an information variable.</span></span>

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

### <span data-ttu-id="4d29d-126">-InstanceSize</span><span class="sxs-lookup"><span data-stu-id="4d29d-126">-InstanceSize</span></span>
<span data-ttu-id="4d29d-127">Указывает имя размера роли, например: ExtraSmall, малый, крупный, ExtraLarge, A5, A6, A7.</span><span class="sxs-lookup"><span data-stu-id="4d29d-127">Specifies the role size name, for example: ExtraSmall, Small, Large, ExtraLarge, A5, A6, A7.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4d29d-128">-Profile</span><span class="sxs-lookup"><span data-stu-id="4d29d-128">-Profile</span></span>
<span data-ttu-id="4d29d-129">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="4d29d-129">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="4d29d-130">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="4d29d-130">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="4d29d-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4d29d-131">CommonParameters</span></span>
<span data-ttu-id="4d29d-132">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="4d29d-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4d29d-133">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4d29d-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4d29d-134">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="4d29d-134">INPUTS</span></span>

## <span data-ttu-id="4d29d-135">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="4d29d-135">OUTPUTS</span></span>

## <span data-ttu-id="4d29d-136">Пуск</span><span class="sxs-lookup"><span data-stu-id="4d29d-136">NOTES</span></span>

## <span data-ttu-id="4d29d-137">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="4d29d-137">RELATED LINKS</span></span>

[<span data-ttu-id="4d29d-138">Get-AzureRole</span><span class="sxs-lookup"><span data-stu-id="4d29d-138">Get-AzureRole</span></span>](./Get-AzureRole.md)

[<span data-ttu-id="4d29d-139">Get-AzureService</span><span class="sxs-lookup"><span data-stu-id="4d29d-139">Get-AzureService</span></span>](./Get-AzureService.md)

[<span data-ttu-id="4d29d-140">Get-AzureVM</span><span class="sxs-lookup"><span data-stu-id="4d29d-140">Get-AzureVM</span></span>](./Get-AzureVM.md)


