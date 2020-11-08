---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: 78DE0AD2-6210-4604-89A8-41915D58BD68
online version: ''
schema: 2.0.0
ms.openlocfilehash: 3c40cb0fd38953ff46fa1138dc91f0b9e97ece75
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94075576"
---
# <span data-ttu-id="b398b-101">Get-AzureSiteRecoveryStorage</span><span class="sxs-lookup"><span data-stu-id="b398b-101">Get-AzureSiteRecoveryStorage</span></span>

## <span data-ttu-id="b398b-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="b398b-102">SYNOPSIS</span></span>
<span data-ttu-id="b398b-103">Получение хранилища для восстановления сайта для хранилища.</span><span class="sxs-lookup"><span data-stu-id="b398b-103">Gets Site Recovery Storages for a vault.</span></span>

## <span data-ttu-id="b398b-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="b398b-104">SYNTAX</span></span>

```
Get-AzureSiteRecoveryStorage -Server <ASRServer> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="b398b-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b398b-105">DESCRIPTION</span></span>
<span data-ttu-id="b398b-106">Командлет **Get-AzureSiteRecoveryStorage** Получает хранилище Azure Site Recovery для текущего хранилища Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="b398b-106">The **Get-AzureSiteRecoveryStorage** cmdlet gets Azure Site Recovery Storages for the current Azure Site Recovery vault.</span></span>

## <span data-ttu-id="b398b-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="b398b-107">EXAMPLES</span></span>

### <span data-ttu-id="b398b-108">Пример 1: Получение хранилища для восстановления сайта</span><span class="sxs-lookup"><span data-stu-id="b398b-108">Example 1: Get site recovery storage</span></span>
```
PS C:\> $Servers = Get-AzureSiteRecoveryServer
PS C:\> Get-AzureSiteRecoveryStorage -Server $Servers[0]
Name           : phase2PrimaryStorageClassification
ID             : 1c1d0c0b-0c50-4675-af1a-1fdac70dbb6d
FabricObjectID : 1c1d0c0b-0c50-4675-af1a-1fdac70dbb6d
ServerId       : 774859b0-1966-48cc-9df7-759c441b7a8c
Type           : Classification
FabricType     : VMM

Name           : phase2RecoveryStorageClassification
ID             : 20cf8d92-fd5d-4872-985a-0f4562b8a0bf
FabricObjectID : 20cf8d92-fd5d-4872-985a-0f4562b8a0bf
ServerId       : 774859b0-1966-48cc-9df7-759c441b7a8c
Type           : Classification
FabricType     : VMM
```

<span data-ttu-id="b398b-109">Первый командлет команды получает серверы для текущего хранилища Azure Site Recovery с помощью командлета **Get-AzureSiteRecoveryServer** .</span><span class="sxs-lookup"><span data-stu-id="b398b-109">The first command cmdlet gets servers for the current Azure Site Recovery vault by using the **Get-AzureSiteRecoveryServer** cmdlet.</span></span>
<span data-ttu-id="b398b-110">Команда хранит серверы восстановления сайта в переменной массива $Servers.</span><span class="sxs-lookup"><span data-stu-id="b398b-110">The command stores the Site Recovery servers in the $Servers array variable.</span></span>

<span data-ttu-id="b398b-111">Вторая команда возвращает хранилище для восстановления сайта первого сервера в массиве $Servers.</span><span class="sxs-lookup"><span data-stu-id="b398b-111">The second command gets the site recovery storage for the first server in the $Servers array.</span></span>

## <span data-ttu-id="b398b-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="b398b-112">PARAMETERS</span></span>

### <span data-ttu-id="b398b-113">-Profile</span><span class="sxs-lookup"><span data-stu-id="b398b-113">-Profile</span></span>
<span data-ttu-id="b398b-114">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="b398b-114">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="b398b-115">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="b398b-115">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="b398b-116">-Сервер</span><span class="sxs-lookup"><span data-stu-id="b398b-116">-Server</span></span>
<span data-ttu-id="b398b-117">Указывает сервер для хранилища Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="b398b-117">Specifies a server for Azure Site Recovery Storage.</span></span>
<span data-ttu-id="b398b-118">Чтобы получить объект **ASRServer** , используйте командлет **Get-AzureSiteRecoveryServer** .</span><span class="sxs-lookup"><span data-stu-id="b398b-118">To obtain an **ASRServer** object, use the **Get-AzureSiteRecoveryServer** cmdlet.</span></span>

```yaml
Type: ASRServer
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b398b-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b398b-119">CommonParameters</span></span>
<span data-ttu-id="b398b-120">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="b398b-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b398b-121">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b398b-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b398b-122">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="b398b-122">INPUTS</span></span>

## <span data-ttu-id="b398b-123">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="b398b-123">OUTPUTS</span></span>

## <span data-ttu-id="b398b-124">Пуск</span><span class="sxs-lookup"><span data-stu-id="b398b-124">NOTES</span></span>

## <span data-ttu-id="b398b-125">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b398b-125">RELATED LINKS</span></span>

[<span data-ttu-id="b398b-126">Get-AzureSiteRecoveryServer</span><span class="sxs-lookup"><span data-stu-id="b398b-126">Get-AzureSiteRecoveryServer</span></span>](./Get-AzureSiteRecoveryServer.md)


