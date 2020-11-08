---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: 0A1FD05F-6573-46D8-8217-C7EA432F6742
online version: ''
schema: 2.0.0
ms.openlocfilehash: fd8ccb634c313f487b6777a9fcb66d872b35510e
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94076109"
---
# <span data-ttu-id="1c93e-101">Remove-AzureSiteRecoveryStorageMapping</span><span class="sxs-lookup"><span data-stu-id="1c93e-101">Remove-AzureSiteRecoveryStorageMapping</span></span>

## <span data-ttu-id="1c93e-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="1c93e-102">SYNOPSIS</span></span>
<span data-ttu-id="1c93e-103">Удаляет сопоставление объекта хранилища для хранилища сайта.</span><span class="sxs-lookup"><span data-stu-id="1c93e-103">Removes a Storage object mapping for a Site Recovery vault.</span></span>

## <span data-ttu-id="1c93e-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="1c93e-104">SYNTAX</span></span>

```
Remove-AzureSiteRecoveryStorageMapping -StorageMapping <ASRStorageMapping> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="1c93e-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="1c93e-105">DESCRIPTION</span></span>
<span data-ttu-id="1c93e-106">Командлет **Remove-AzureSiteRecoveryStorageMapping** удаляет сопоставление объектов хранилища для текущего хранилища Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="1c93e-106">The **Remove-AzureSiteRecoveryStorageMapping** cmdlet removes a Storage object mapping for the current Azure Site Recovery vault.</span></span>

## <span data-ttu-id="1c93e-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="1c93e-107">EXAMPLES</span></span>

### <span data-ttu-id="1c93e-108">Пример 1: Удаление сопоставления между сетью и сетью восстановления</span><span class="sxs-lookup"><span data-stu-id="1c93e-108">Example 1: Remove the mapping between a network and a recovery network</span></span>
```
PS C:\> $Servers = Get-AzureSiteRecoveryServer
PS C:\> $StorageMapping = Get-AzureSiteRecoveryStorageMapping -PrimaryServer $Servers[0] -RecoveryServer $Servers[1]
PS C:\> Remove-AzureSiteRecoveryStorageMapping -StorageMapping $StorageMapping
Get-AzureSiteRecoveryServerGet-AzureSiteRecoveryStorageMappingNew-AzureSiteRecoveryStorageMapping
```

<span data-ttu-id="1c93e-109">Первый командлет команды получает серверы для текущего хранилища Azure Site Recovery с помощью командлета **Get-AzureSiteRecoveryServer** .</span><span class="sxs-lookup"><span data-stu-id="1c93e-109">The first command cmdlet gets servers for the current Azure Site Recovery vault by using the **Get-AzureSiteRecoveryServer** cmdlet.</span></span>
<span data-ttu-id="1c93e-110">Команда хранит серверы восстановления сайта в переменной массива $Servers.</span><span class="sxs-lookup"><span data-stu-id="1c93e-110">The command stores the Site Recovery servers in the $Servers array variable.</span></span>

<span data-ttu-id="1c93e-111">Вторая команда получает сопоставление между двумя объектами хранилища, а затем сохраняет их в переменной $StorageMapping.</span><span class="sxs-lookup"><span data-stu-id="1c93e-111">The second command gets the mapping between two Storage objects, and then stores it in the $StorageMapping variable.</span></span>
<span data-ttu-id="1c93e-112">Команда задает основной сервер для сетевого сопоставления в качестве первого элемента $Servers.</span><span class="sxs-lookup"><span data-stu-id="1c93e-112">The command specifies the primary server for the network mapping as the first element of $Servers.</span></span>
<span data-ttu-id="1c93e-113">Команда задает сервер для сети восстановления во втором элементе $Servers.</span><span class="sxs-lookup"><span data-stu-id="1c93e-113">The command specifies the server for the recovery network as the second element of $Servers.</span></span>

<span data-ttu-id="1c93e-114">Последняя команда удаляет сопоставление в $StorageMapping.</span><span class="sxs-lookup"><span data-stu-id="1c93e-114">The final command removes the mapping in $StorageMapping.</span></span>

## <span data-ttu-id="1c93e-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="1c93e-115">PARAMETERS</span></span>

### <span data-ttu-id="1c93e-116">-Profile</span><span class="sxs-lookup"><span data-stu-id="1c93e-116">-Profile</span></span>
<span data-ttu-id="1c93e-117">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="1c93e-117">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="1c93e-118">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="1c93e-118">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="1c93e-119">-StorageMapping</span><span class="sxs-lookup"><span data-stu-id="1c93e-119">-StorageMapping</span></span>
<span data-ttu-id="1c93e-120">Указывает сетевое сопоставление.</span><span class="sxs-lookup"><span data-stu-id="1c93e-120">Specifies a network mapping.</span></span>
<span data-ttu-id="1c93e-121">Чтобы получить **ASRStorageMapping** , используйте командлет **Get-AzureSiteRecoveryStorage** .</span><span class="sxs-lookup"><span data-stu-id="1c93e-121">To obtain an **ASRStorageMapping** , use the **Get-AzureSiteRecoveryStorage** cmdlet.</span></span>

```yaml
Type: ASRStorageMapping
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1c93e-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1c93e-122">CommonParameters</span></span>
<span data-ttu-id="1c93e-123">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="1c93e-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1c93e-124">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1c93e-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1c93e-125">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="1c93e-125">INPUTS</span></span>

## <span data-ttu-id="1c93e-126">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="1c93e-126">OUTPUTS</span></span>

## <span data-ttu-id="1c93e-127">Пуск</span><span class="sxs-lookup"><span data-stu-id="1c93e-127">NOTES</span></span>

## <span data-ttu-id="1c93e-128">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="1c93e-128">RELATED LINKS</span></span>

[<span data-ttu-id="1c93e-129">Get-AzureSiteRecoveryStorage</span><span class="sxs-lookup"><span data-stu-id="1c93e-129">Get-AzureSiteRecoveryStorage</span></span>](./Get-AzureSiteRecoveryStorage.md)


