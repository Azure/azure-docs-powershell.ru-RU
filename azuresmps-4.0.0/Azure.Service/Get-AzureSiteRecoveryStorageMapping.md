---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: 4F083EBC-7D7E-4836-8AAB-6BF2B08162DF
online version: ''
schema: 2.0.0
ms.openlocfilehash: 6a69d54b315319e3dacc150edc2a8737be9b96e3
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94075575"
---
# <span data-ttu-id="b86b1-101">Get-AzureSiteRecoveryStorageMapping</span><span class="sxs-lookup"><span data-stu-id="b86b1-101">Get-AzureSiteRecoveryStorageMapping</span></span>

## <span data-ttu-id="b86b1-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="b86b1-102">SYNOPSIS</span></span>
<span data-ttu-id="b86b1-103">Возвращает сопоставления объектов хранилища для восстановления сайта для хранилища.</span><span class="sxs-lookup"><span data-stu-id="b86b1-103">Gets mappings of Site Recovery Storage objects for a vault.</span></span>

## <span data-ttu-id="b86b1-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="b86b1-104">SYNTAX</span></span>

```
Get-AzureSiteRecoveryStorageMapping -PrimaryServer <ASRServer> -RecoveryServer <ASRServer>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="b86b1-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b86b1-105">DESCRIPTION</span></span>
<span data-ttu-id="b86b1-106">Командлет **Get-AzureSiteRecoveryStorageMapping** получает сопоставление объектов хранилища Azure Site Recovery для текущего хранилища Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="b86b1-106">The **Get-AzureSiteRecoveryStorageMapping** cmdlet gets mappings of Azure Site Recovery Storage objects for the current Azure Site Recovery vault.</span></span>

## <span data-ttu-id="b86b1-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="b86b1-107">EXAMPLES</span></span>

### <span data-ttu-id="b86b1-108">Пример 1: получение сопоставления между объектом хранилища и объектом хранилища для восстановления</span><span class="sxs-lookup"><span data-stu-id="b86b1-108">Example 1: Get the mapping between a Storage object and a recovery Storage object</span></span>
```
PS C:\> $Servers = Get-AzureSiteRecoveryServer
PS C:\> Get-AzureSiteRecoveryStorageMapping -PrimaryServer $Servers[0] -RecoveryServer $Servers[1]
PrimaryServerId     : 774859b0-1966-48cc-9df7-759c441b7a8c
PrimaryStorageId    : 1c1d0c0b-0c50-4675-af1a-1fdac70dbb6d
PrimaryStorageName  : phase2PrimaryStorageClassification
RecoveryServerId    : 774859b0-1966-48cc-9df7-759c441b7a8c
RecoveryStorageId   : 20cf8d92-fd5d-4872-985a-0f4562b8a0bf
RecoveryStorageName : phase2RecoveryStorageClassification
```

<span data-ttu-id="b86b1-109">Первый командлет команды получает серверы для текущего хранилища Azure Site Recovery с помощью командлета **Get-AzureSiteRecoveryServer** .</span><span class="sxs-lookup"><span data-stu-id="b86b1-109">The first command cmdlet gets servers for the current Azure Site Recovery vault by using the **Get-AzureSiteRecoveryServer** cmdlet.</span></span>
<span data-ttu-id="b86b1-110">Команда хранит серверы восстановления сайта в переменной массива $Servers.</span><span class="sxs-lookup"><span data-stu-id="b86b1-110">The command stores the Site Recovery servers in the $Servers array variable.</span></span>

<span data-ttu-id="b86b1-111">Вторая команда получает сопоставление между двумя объектами хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="b86b1-111">The second command gets the mapping between two Azure Storage objects.</span></span>
<span data-ttu-id="b86b1-112">Команда задает основной сервер для сопоставления объектов хранилища в первом элементе $Servers.</span><span class="sxs-lookup"><span data-stu-id="b86b1-112">The command specifies the primary server for the Storage object mapping as the first element of $Servers.</span></span>
<span data-ttu-id="b86b1-113">Команда задает сервер для объекта хранилища для восстановления в качестве второго элемента $Servers.</span><span class="sxs-lookup"><span data-stu-id="b86b1-113">The command specifies the server for the recovery Storage object as the second element of $Servers.</span></span>

## <span data-ttu-id="b86b1-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="b86b1-114">PARAMETERS</span></span>

### <span data-ttu-id="b86b1-115">-PrimaryServer</span><span class="sxs-lookup"><span data-stu-id="b86b1-115">-PrimaryServer</span></span>
<span data-ttu-id="b86b1-116">Указывает основной сервер.</span><span class="sxs-lookup"><span data-stu-id="b86b1-116">Specifies the primary server.</span></span>
<span data-ttu-id="b86b1-117">Чтобы получить сервер, используйте командлет **Get-AzureSiteRecoveryServer** .</span><span class="sxs-lookup"><span data-stu-id="b86b1-117">To obtain a server, use the **Get-AzureSiteRecoveryServer** cmdlet.</span></span>

```yaml
Type: ASRServer
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b86b1-118">-Profile</span><span class="sxs-lookup"><span data-stu-id="b86b1-118">-Profile</span></span>
<span data-ttu-id="b86b1-119">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="b86b1-119">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="b86b1-120">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="b86b1-120">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="b86b1-121">-RecoveryServer</span><span class="sxs-lookup"><span data-stu-id="b86b1-121">-RecoveryServer</span></span>
<span data-ttu-id="b86b1-122">Указывает сервер восстановления.</span><span class="sxs-lookup"><span data-stu-id="b86b1-122">Specifies the recovery server.</span></span>
<span data-ttu-id="b86b1-123">Чтобы получить сервер, используйте **Get-AzureSiteRecoveryServer**.</span><span class="sxs-lookup"><span data-stu-id="b86b1-123">To obtain a server, use **Get-AzureSiteRecoveryServer**.</span></span>

```yaml
Type: ASRServer
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b86b1-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b86b1-124">CommonParameters</span></span>
<span data-ttu-id="b86b1-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="b86b1-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b86b1-126">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b86b1-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b86b1-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="b86b1-127">INPUTS</span></span>

## <span data-ttu-id="b86b1-128">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="b86b1-128">OUTPUTS</span></span>

## <span data-ttu-id="b86b1-129">Пуск</span><span class="sxs-lookup"><span data-stu-id="b86b1-129">NOTES</span></span>

## <span data-ttu-id="b86b1-130">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b86b1-130">RELATED LINKS</span></span>

[<span data-ttu-id="b86b1-131">Get-AzureSiteRecoveryServer</span><span class="sxs-lookup"><span data-stu-id="b86b1-131">Get-AzureSiteRecoveryServer</span></span>](./Get-AzureSiteRecoveryServer.md)

[<span data-ttu-id="b86b1-132">New-AzureSiteRecoveryStorageMapping</span><span class="sxs-lookup"><span data-stu-id="b86b1-132">New-AzureSiteRecoveryStorageMapping</span></span>](./New-AzureSiteRecoveryStorageMapping.md)

[<span data-ttu-id="b86b1-133">Remove-AzureSiteRecoveryStorageMapping</span><span class="sxs-lookup"><span data-stu-id="b86b1-133">Remove-AzureSiteRecoveryStorageMapping</span></span>](./Remove-AzureSiteRecoveryStorageMapping.md)


