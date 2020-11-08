---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: 16146A0D-4605-489A-8259-A37BEAC98306
online version: ''
schema: 2.0.0
ms.openlocfilehash: 664c9af9373120f293153a1bbdc65d1a82637631
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94076015"
---
# <span data-ttu-id="5e558-101">Update-AzureSiteRecoveryProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="5e558-101">Update-AzureSiteRecoveryProtectionEntity</span></span>

## <span data-ttu-id="5e558-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="5e558-102">SYNOPSIS</span></span>
<span data-ttu-id="5e558-103">Обновляет свойства сущности "Защита" в Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="5e558-103">Updates the properties of a protection entity in Azure Site Recovery.</span></span>

## <span data-ttu-id="5e558-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="5e558-104">SYNTAX</span></span>

```
Update-AzureSiteRecoveryProtectionEntity -ProtectionEntity <ASRProtectionEntity> [-WaitForCompletion]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="5e558-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="5e558-105">DESCRIPTION</span></span>
<span data-ttu-id="5e558-106">Командлет **Update-AzureSiteRecoveryProtectionEntity** обновляет свойства сущности защиты в Azure Site Recovery, например сведения о владельце виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="5e558-106">The **Update-AzureSiteRecoveryProtectionEntity** cmdlet updates the properties of a protection entity in Azure Site Recovery, such as virtual machine owner information.</span></span>
<span data-ttu-id="5e558-107">Этот командлет поддерживается только для мониторов виртуальных машин (VMM), защищенных от VMM.</span><span class="sxs-lookup"><span data-stu-id="5e558-107">This cmdlet is supported only for Virtual Machine Monitor (VMM) to VMM protected protection entities.</span></span>

## <span data-ttu-id="5e558-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="5e558-108">EXAMPLES</span></span>

### <span data-ttu-id="5e558-109">Пример 1: обновление объекта защиты</span><span class="sxs-lookup"><span data-stu-id="5e558-109">Example 1: Update a protection entity</span></span>
```
PS C:\> $Container = Get-AzureSiteRecoveryProtectionContainer
PS C:\> $ProtectionEntity = Get-AzureSiteRecoveryProtectionEntity -ProtectionContainer $Container
PS C:\> Update-AzureSiteRecoveryProtectionEntity -ProtectionEntity $ProtectionEntity
           Name             : 
           ID               : 680ffe0f-6236-465e-8c94-81242fa67e6d
           ClientRequestId  : 2c47e6ce-1460-4187-8a0f-b9073735fa38-2014-12-30 06:44:40Z-P
           State            : NotStarted
           StateDescription : NotStarted
           StartTime        : 
           EndTime          : 
           AllowedActions   : {}
           Tasks            : {}
           Errors           : {}
```

<span data-ttu-id="5e558-110">Первая команда получает защищенный контейнер с помощью командлета **Get-AzureSiteRecoveryProtectionContainer** , а затем сохраняет этот объект в переменной $Container.</span><span class="sxs-lookup"><span data-stu-id="5e558-110">The first command gets a protected container by using the **Get-AzureSiteRecoveryProtectionContainer** cmdlet, and then stores that object in the $Container variable.</span></span>

<span data-ttu-id="5e558-111">Вторая команда получает защищенную виртуальную машину, которая относится к контейнеру, хранящемуся в $Container, с помощью командлета **Get-AzureSiteRecoveryProtectionEntity** , а затем сохраняет его в переменной $ProtectionEntity.</span><span class="sxs-lookup"><span data-stu-id="5e558-111">The second command gets the protected virtual machine that belongs to the container stored in $Container by using the **Get-AzureSiteRecoveryProtectionEntity** cmdlet, and then stores it in the $ProtectionEntity variable.</span></span>

<span data-ttu-id="5e558-112">Последняя команда обновляет объект защиты в $ProtectionEntity.</span><span class="sxs-lookup"><span data-stu-id="5e558-112">The final command updates the protection entity in $ProtectionEntity.</span></span>

## <span data-ttu-id="5e558-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="5e558-113">PARAMETERS</span></span>

### <span data-ttu-id="5e558-114">-Profile</span><span class="sxs-lookup"><span data-stu-id="5e558-114">-Profile</span></span>
<span data-ttu-id="5e558-115">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="5e558-115">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="5e558-116">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="5e558-116">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="5e558-117">-ProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="5e558-117">-ProtectionEntity</span></span>
<span data-ttu-id="5e558-118">Указывает сущность защиты для обновления.</span><span class="sxs-lookup"><span data-stu-id="5e558-118">Specifies a protection entity to update.</span></span>
<span data-ttu-id="5e558-119">Чтобы получить объект **ASRProtectionEntity** , используйте командлет **Get-AzureSiteRecoveryProtectionEntity** .</span><span class="sxs-lookup"><span data-stu-id="5e558-119">To obtain an **ASRProtectionEntity** object, use the **Get-AzureSiteRecoveryProtectionEntity** cmdlet.</span></span>

```yaml
Type: ASRProtectionEntity
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5e558-120">-WaitForCompletion</span><span class="sxs-lookup"><span data-stu-id="5e558-120">-WaitForCompletion</span></span>
<span data-ttu-id="5e558-121">Указывает на то, что этот командлет ожидает завершения операции до того, как она возвратит управление на консоль Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="5e558-121">Indicates that this cmdlet waits for the operation to complete before it returns control to the Windows PowerShell console.</span></span>

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

### <span data-ttu-id="5e558-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5e558-122">CommonParameters</span></span>
<span data-ttu-id="5e558-123">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="5e558-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5e558-124">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5e558-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5e558-125">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="5e558-125">INPUTS</span></span>

## <span data-ttu-id="5e558-126">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="5e558-126">OUTPUTS</span></span>

## <span data-ttu-id="5e558-127">Пуск</span><span class="sxs-lookup"><span data-stu-id="5e558-127">NOTES</span></span>

## <span data-ttu-id="5e558-128">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="5e558-128">RELATED LINKS</span></span>

[<span data-ttu-id="5e558-129">Get-AzureSiteRecoveryProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="5e558-129">Get-AzureSiteRecoveryProtectionContainer</span></span>](./Get-AzureSiteRecoveryProtectionContainer.md)

[<span data-ttu-id="5e558-130">Get-AzureSiteRecoveryProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="5e558-130">Get-AzureSiteRecoveryProtectionEntity</span></span>](./Get-AzureSiteRecoveryProtectionEntity.md)

[<span data-ttu-id="5e558-131">Set-AzureSiteRecoveryProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="5e558-131">Set-AzureSiteRecoveryProtectionEntity</span></span>](./Set-AzureSiteRecoveryProtectionEntity.md)


