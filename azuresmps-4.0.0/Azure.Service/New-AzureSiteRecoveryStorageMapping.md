---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: 2D09422F-82B1-4243-B835-8BF223A6F936
online version: ''
schema: 2.0.0
ms.openlocfilehash: a6f02f333601172341de4fe8a0bf629037f712a5
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94075975"
---
# <span data-ttu-id="9a0a6-101">New-AzureSiteRecoveryStorageMapping</span><span class="sxs-lookup"><span data-stu-id="9a0a6-101">New-AzureSiteRecoveryStorageMapping</span></span>

## <span data-ttu-id="9a0a6-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="9a0a6-102">SYNOPSIS</span></span>
<span data-ttu-id="9a0a6-103">Создание сопоставления между объектом хранилища Azure и объектом хранилища для восстановления.</span><span class="sxs-lookup"><span data-stu-id="9a0a6-103">Creates a mapping between an Azure Storage object and recovery Storage object.</span></span>

## <span data-ttu-id="9a0a6-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="9a0a6-104">SYNTAX</span></span>

```
New-AzureSiteRecoveryStorageMapping -PrimaryStorage <ASRStorage> -RecoveryStorage <ASRStorage>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="9a0a6-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="9a0a6-105">DESCRIPTION</span></span>
<span data-ttu-id="9a0a6-106">Командлет **New-AzureSiteRecoveryStorageMapping** создает сопоставление между объектом Azure Site Recovery, управляемым базой данных Azure и объектом хранилища для восстановления.</span><span class="sxs-lookup"><span data-stu-id="9a0a6-106">The **New-AzureSiteRecoveryStorageMapping** cmdlet creates a mapping between an Azure Site Recovery managed primary Azure Storage object and a recovery Storage object.</span></span>

## <span data-ttu-id="9a0a6-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="9a0a6-107">EXAMPLES</span></span>

### <span data-ttu-id="9a0a6-108">Пример 1: Создание сопоставления между объектом хранилища и объектом хранилища для восстановления</span><span class="sxs-lookup"><span data-stu-id="9a0a6-108">Example 1: Create a mapping between a storage object and a recovery storage object</span></span>
```
PS C:\> $Servers = Get-AzureSiteRecoveryServer
PS C:\> $Storages = Get-AzureSiteRecoveryStorage -Server $Servers[0]
PS C:\> New-AzureSiteRecoveryStorageMapping -PrimaryStorage $Storages[0] -RecoveryStorage $Storages[1]
```

<span data-ttu-id="9a0a6-109">Первый командлет команды получает серверы для текущего хранилища Azure Site Recovery с помощью командлета **Get-AzureSiteRecoveryServer** .</span><span class="sxs-lookup"><span data-stu-id="9a0a6-109">The first command cmdlet gets servers for the current Azure Site Recovery vault by using the **Get-AzureSiteRecoveryServer** cmdlet.</span></span>
<span data-ttu-id="9a0a6-110">Команда хранит серверы восстановления сайта в переменной массива $Servers.</span><span class="sxs-lookup"><span data-stu-id="9a0a6-110">The command stores the Site Recovery servers in the $Servers array variable.</span></span>

<span data-ttu-id="9a0a6-111">Вторая команда получает хранилище для восстановления сайта для первого сервера в массиве $Servers и сохраняет его в $Storages.</span><span class="sxs-lookup"><span data-stu-id="9a0a6-111">The second command gets the site recovery storage for the first server in the $Servers array, and then stores it in the $Storages.</span></span>

<span data-ttu-id="9a0a6-112">Последняя команда создает сопоставление между основной сетью и сетью восстановления.</span><span class="sxs-lookup"><span data-stu-id="9a0a6-112">The final command creates a mapping between the primary network and the recovery network.</span></span>
<span data-ttu-id="9a0a6-113">Команда задает Первичный объект хранилища в качестве первого элемента $Storages.</span><span class="sxs-lookup"><span data-stu-id="9a0a6-113">The command specifies the primary Storage object as the first element of $Storages.</span></span>
<span data-ttu-id="9a0a6-114">Команда задает объект хранилища для восстановления в качестве второго элемента $Storages.</span><span class="sxs-lookup"><span data-stu-id="9a0a6-114">The command specifies the recovery Storage object as the second element of $Storages.</span></span>

## <span data-ttu-id="9a0a6-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="9a0a6-115">PARAMETERS</span></span>

### <span data-ttu-id="9a0a6-116">-PrimaryStorage</span><span class="sxs-lookup"><span data-stu-id="9a0a6-116">-PrimaryStorage</span></span>
<span data-ttu-id="9a0a6-117">Задает основное хранилище для сопоставления с хранилищем для восстановления.</span><span class="sxs-lookup"><span data-stu-id="9a0a6-117">Specifies the primary Storage to map to the recovery Storage.</span></span>
<span data-ttu-id="9a0a6-118">Чтобы получить объект **ASRStorage** , используйте командлет Get-AzureSiteRecoveryStorage.</span><span class="sxs-lookup"><span data-stu-id="9a0a6-118">To obtain an **ASRStorage** object, use the Get-AzureSiteRecoveryStorage cmdlet.</span></span>

```yaml
Type: ASRStorage
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9a0a6-119">-Profile</span><span class="sxs-lookup"><span data-stu-id="9a0a6-119">-Profile</span></span>
<span data-ttu-id="9a0a6-120">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="9a0a6-120">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="9a0a6-121">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="9a0a6-121">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="9a0a6-122">-RecoveryStorage</span><span class="sxs-lookup"><span data-stu-id="9a0a6-122">-RecoveryStorage</span></span>
<span data-ttu-id="9a0a6-123">Указывает объект хранилища для восстановления.</span><span class="sxs-lookup"><span data-stu-id="9a0a6-123">Specifies the recovery Storage object.</span></span>
<span data-ttu-id="9a0a6-124">Этот командлет сопоставляет основной объект хранилища объекту хранилища, указанному в этом параметре.</span><span class="sxs-lookup"><span data-stu-id="9a0a6-124">This cmdlet maps the primary Storage object to the Storage object that this parameter specifies.</span></span>
<span data-ttu-id="9a0a6-125">Чтобы получить объект **ASRStorage** , используйте **Get-AzureSiteRecoveryStorage**.</span><span class="sxs-lookup"><span data-stu-id="9a0a6-125">To obtain an **ASRStorage** object, use **Get-AzureSiteRecoveryStorage**.</span></span>

```yaml
Type: ASRStorage
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9a0a6-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9a0a6-126">CommonParameters</span></span>
<span data-ttu-id="9a0a6-127">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="9a0a6-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9a0a6-128">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9a0a6-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9a0a6-129">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="9a0a6-129">INPUTS</span></span>

## <span data-ttu-id="9a0a6-130">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="9a0a6-130">OUTPUTS</span></span>

## <span data-ttu-id="9a0a6-131">Пуск</span><span class="sxs-lookup"><span data-stu-id="9a0a6-131">NOTES</span></span>

## <span data-ttu-id="9a0a6-132">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="9a0a6-132">RELATED LINKS</span></span>

[<span data-ttu-id="9a0a6-133">Get-AzureSiteRecoveryStorage</span><span class="sxs-lookup"><span data-stu-id="9a0a6-133">Get-AzureSiteRecoveryStorage</span></span>](./Get-AzureSiteRecoveryStorage.md)

[<span data-ttu-id="9a0a6-134">Get-AzureSiteRecoveryStorageMapping</span><span class="sxs-lookup"><span data-stu-id="9a0a6-134">Get-AzureSiteRecoveryStorageMapping</span></span>](./Get-AzureSiteRecoveryStorageMapping.md)

[<span data-ttu-id="9a0a6-135">Remove-AzureSiteRecoveryStorageMapping</span><span class="sxs-lookup"><span data-stu-id="9a0a6-135">Remove-AzureSiteRecoveryStorageMapping</span></span>](./Remove-AzureSiteRecoveryStorageMapping.md)


