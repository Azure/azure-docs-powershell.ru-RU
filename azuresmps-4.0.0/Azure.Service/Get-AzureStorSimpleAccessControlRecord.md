---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: 71302FB6-7E2B-4972-A743-AB537AC7CD79
online version: ''
schema: 2.0.0
ms.openlocfilehash: 79e194e0f8dda4392dec191881702c680bf172ac
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94076552"
---
# <span data-ttu-id="ab9cc-101">Get-AzureStorSimpleAccessControlRecord</span><span class="sxs-lookup"><span data-stu-id="ab9cc-101">Get-AzureStorSimpleAccessControlRecord</span></span>

## <span data-ttu-id="ab9cc-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="ab9cc-102">SYNOPSIS</span></span>
<span data-ttu-id="ab9cc-103">Возвращает записи управления доступом в конфигурации службы.</span><span class="sxs-lookup"><span data-stu-id="ab9cc-103">Gets access control records in a service configuration.</span></span>

## <span data-ttu-id="ab9cc-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="ab9cc-104">SYNTAX</span></span>

```
Get-AzureStorSimpleAccessControlRecord [-ACRName <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="ab9cc-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ab9cc-105">DESCRIPTION</span></span>
<span data-ttu-id="ab9cc-106">Командлет **Get-AzureStorSimpleAccessControlRecord** получает записи управления доступом в конфигурации службы StorSimple Manager.</span><span class="sxs-lookup"><span data-stu-id="ab9cc-106">The **Get-AzureStorSimpleAccessControlRecord** cmdlet gets access control records in the StorSimple Manager service configuration.</span></span>
<span data-ttu-id="ab9cc-107">Этот командлет получает все записи или именованную запись.</span><span class="sxs-lookup"><span data-stu-id="ab9cc-107">This cmdlet gets all records or a named record.</span></span>

<span data-ttu-id="ab9cc-108">Записи управления доступом — это контейнеры параметров инициатора iSCSI.</span><span class="sxs-lookup"><span data-stu-id="ab9cc-108">Access control records are containers of iSCSI initiator parameters.</span></span>
<span data-ttu-id="ab9cc-109">Эти параметры определяют, какие инициаторы могут получать доступ к тому.</span><span class="sxs-lookup"><span data-stu-id="ab9cc-109">These parameters specify which initiators can access a volume.</span></span>
<span data-ttu-id="ab9cc-110">Когда инициатор iSCSI пытается подключиться к тому, устройство проверяет записи управления доступом, назначенные этому тому.</span><span class="sxs-lookup"><span data-stu-id="ab9cc-110">When an iSCSI initiator attempts to connect to a volume, your appliance checks the access control records assigned to that volume.</span></span>
<span data-ttu-id="ab9cc-111">Если инициатор iSCSI соответствует одной из записей в записи управления доступом, сопоставленных с этим томом, инициатор iSCSI может подключиться.</span><span class="sxs-lookup"><span data-stu-id="ab9cc-111">If the iSCSI initiator parameters match one of the entries in an access control record mapped to that volume, the iSCSI initiator can connect.</span></span>

## <span data-ttu-id="ab9cc-112">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="ab9cc-112">EXAMPLES</span></span>

### <span data-ttu-id="ab9cc-113">Пример 1: получение всех записей контроля доступа</span><span class="sxs-lookup"><span data-stu-id="ab9cc-113">Example 1: Get all access control records</span></span>
```
PS C:\>Get-AzureStorSimpleAccessControlRecord
InstanceId                           Name                        InitiatorName               VolumeCount
----------                           ----                        -------------               -----------
01a31aa5-14de-4b77-b926-2842577f540e Windows_XYUSFL718-RV_ACR    iqn.1991-05.com.microsof... 3
071c282d-0cd2-4c5f-b687-48966037ba48 Linux_XYUSFL719_ACR         iqn.1994-05.com.redhat:a... 3
4600eade-71f8-4d04-baec-0e7cf1d1e8fb Windows_XYUSFL720_ACR       iqn.1991-05.com.microsof... 9
d508d6f0-fcda-4624-b223-c0b307d6113e Linux_XYUSFL350_ACR         iqn.1991-05.com.microsof... 9
```

<span data-ttu-id="ab9cc-114">Эта команда возвращает все записи управления доступом.</span><span class="sxs-lookup"><span data-stu-id="ab9cc-114">This command gets all access control records.</span></span>

### <span data-ttu-id="ab9cc-115">Пример 2: получение конкретной записи контроля доступа</span><span class="sxs-lookup"><span data-stu-id="ab9cc-115">Example 2: Get a specific access control record</span></span>
```
PS C:\>Get-AzureStorSimpleAccessControlRecord -ACRName "Acr11"
VERBOSE: ClientRequestId: 61f261c7-acd3-4bcc-922a-ddfd85eb767b_PS
VERBOSE: ClientRequestId: 49c6a4c7-d299-46fd-a553-034c52b47487_PS

GlobalId            : 
InitiatorName       : iqn-contoso63
InstanceId          : 55f24643-ab3a-4098-ade2-aa2b1a3ab18c
Name                : Acr11
OperationInProgress : None
VolumeCount         : 6

VERBOSE: Access Control Record with given name Acr11 is found!
```

<span data-ttu-id="ab9cc-116">Эта команда получает запись контроля доступа с именем Acr11.</span><span class="sxs-lookup"><span data-stu-id="ab9cc-116">This command gets the access control record named Acr11.</span></span>

## <span data-ttu-id="ab9cc-117">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="ab9cc-117">PARAMETERS</span></span>

### <span data-ttu-id="ab9cc-118">-ACRName</span><span class="sxs-lookup"><span data-stu-id="ab9cc-118">-ACRName</span></span>
<span data-ttu-id="ab9cc-119">Указывает имя записи контроля доступа, которую требуется получить.</span><span class="sxs-lookup"><span data-stu-id="ab9cc-119">Specifies the name of an access control record to get.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ab9cc-120">-Profile</span><span class="sxs-lookup"><span data-stu-id="ab9cc-120">-Profile</span></span>
<span data-ttu-id="ab9cc-121">Указывает профиль Azure.</span><span class="sxs-lookup"><span data-stu-id="ab9cc-121">Specifies an Azure profile.</span></span>

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

### <span data-ttu-id="ab9cc-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ab9cc-122">CommonParameters</span></span>
<span data-ttu-id="ab9cc-123">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="ab9cc-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ab9cc-124">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ab9cc-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ab9cc-125">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="ab9cc-125">INPUTS</span></span>

### <span data-ttu-id="ab9cc-126">Ничего</span><span class="sxs-lookup"><span data-stu-id="ab9cc-126">None</span></span>

## <span data-ttu-id="ab9cc-127">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="ab9cc-127">OUTPUTS</span></span>

### <span data-ttu-id="ab9cc-128">AccessControlRecord, IList\<AccessControlRecord\></span><span class="sxs-lookup"><span data-stu-id="ab9cc-128">AccessControlRecord, IList\<AccessControlRecord\></span></span>
<span data-ttu-id="ab9cc-129">Этот командлет возвращает объект **AccessControlRecord** или объект **IList \<AccessControlRecord\>** .</span><span class="sxs-lookup"><span data-stu-id="ab9cc-129">This cmdlet returns an **AccessControlRecord** object or an **IList\<AccessControlRecord\>** object.</span></span>
<span data-ttu-id="ab9cc-130">Объект **AccessControlRecord** состоит из следующих полей:</span><span class="sxs-lookup"><span data-stu-id="ab9cc-130">An **AccessControlRecord** object contains the following fields:</span></span> 

- <span data-ttu-id="ab9cc-131">**GlobalId** ( **строка** )</span><span class="sxs-lookup"><span data-stu-id="ab9cc-131">**GlobalId** ( **String** )</span></span> 
- <span data-ttu-id="ab9cc-132">**InitiatorName** ( **строка** )</span><span class="sxs-lookup"><span data-stu-id="ab9cc-132">**InitiatorName** ( **String** )</span></span> 
- <span data-ttu-id="ab9cc-133">**InstanceId** ( **строка** )</span><span class="sxs-lookup"><span data-stu-id="ab9cc-133">**InstanceId** ( **String** )</span></span> 
- <span data-ttu-id="ab9cc-134">**Name** ( **строка** )</span><span class="sxs-lookup"><span data-stu-id="ab9cc-134">**Name** ( **String** )</span></span> 
- <span data-ttu-id="ab9cc-135">**OperationInProgress** ( **OperationInProgress** )</span><span class="sxs-lookup"><span data-stu-id="ab9cc-135">**OperationInProgress** ( **OperationInProgress** )</span></span> 
- <span data-ttu-id="ab9cc-136">**VolumeCount** ( **int** )</span><span class="sxs-lookup"><span data-stu-id="ab9cc-136">**VolumeCount** ( **int** )</span></span>

## <span data-ttu-id="ab9cc-137">Пуск</span><span class="sxs-lookup"><span data-stu-id="ab9cc-137">NOTES</span></span>

## <span data-ttu-id="ab9cc-138">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ab9cc-138">RELATED LINKS</span></span>

[<span data-ttu-id="ab9cc-139">New-AzureStorSimpleAccessControlRecord</span><span class="sxs-lookup"><span data-stu-id="ab9cc-139">New-AzureStorSimpleAccessControlRecord</span></span>](./New-AzureStorSimpleAccessControlRecord.md)

[<span data-ttu-id="ab9cc-140">Remove-AzureStorSimpleAccessControlRecord</span><span class="sxs-lookup"><span data-stu-id="ab9cc-140">Remove-AzureStorSimpleAccessControlRecord</span></span>](./Remove-AzureStorSimpleAccessControlRecord.md)

[<span data-ttu-id="ab9cc-141">Set-AzureStorSimpleAccessControlRecord</span><span class="sxs-lookup"><span data-stu-id="ab9cc-141">Set-AzureStorSimpleAccessControlRecord</span></span>](./Set-AzureStorSimpleAccessControlRecord.md)


