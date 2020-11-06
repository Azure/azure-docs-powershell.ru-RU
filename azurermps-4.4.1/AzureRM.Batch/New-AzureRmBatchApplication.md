---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: FF111B74-90A3-4F7C-B515-CE1EEF68EB54
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/New-AzureRmBatchApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/New-AzureRmBatchApplication.md
ms.openlocfilehash: 6c2ab80f5b9fb38ed2f6399d9f186134f4659edf
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93566310"
---
# <span data-ttu-id="b49fc-101">New-AzureRmBatchApplication</span><span class="sxs-lookup"><span data-stu-id="b49fc-101">New-AzureRmBatchApplication</span></span>

## <span data-ttu-id="b49fc-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="b49fc-102">SYNOPSIS</span></span>
<span data-ttu-id="b49fc-103">Добавляет приложение в указанную учетную запись пакета.</span><span class="sxs-lookup"><span data-stu-id="b49fc-103">Adds an application to the specified Batch account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b49fc-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="b49fc-104">SYNTAX</span></span>

```
New-AzureRmBatchApplication [-AccountName] <String> [-ResourceGroupName] <String> [-ApplicationId] <String>
 [[-AllowUpdates] <Boolean>] [[-DisplayName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="b49fc-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b49fc-105">DESCRIPTION</span></span>
<span data-ttu-id="b49fc-106">Командлет **New-AzureRmBatchApplication** добавляет приложение в указанную учетную запись пакета Azure.</span><span class="sxs-lookup"><span data-stu-id="b49fc-106">The **New-AzureRmBatchApplication** cmdlet adds an application to the specified Azure Batch account.</span></span>

## <span data-ttu-id="b49fc-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="b49fc-107">EXAMPLES</span></span>

### <span data-ttu-id="b49fc-108">Пример 1: Добавление пустого приложения в пакетную учетную запись</span><span class="sxs-lookup"><span data-stu-id="b49fc-108">Example 1: Add an empty application to a Batch account</span></span>
```
PS C:\>New-AzureRmBatchApplication -AccountName "ContosoBatch" -ResourceGroupName "ContosoBatchGroup" -ApplicationId "Litware" -AllowUpdates $True -DisplayName "Litware Advanced Reticulator"
```

<span data-ttu-id="b49fc-109">Эта команда создает приложение беседа Litware в учетной записи ContosoBatch.</span><span class="sxs-lookup"><span data-stu-id="b49fc-109">This command creates the Litware application in the ContosoBatch account.</span></span>
<span data-ttu-id="b49fc-110">Приложение изначально не включает пакеты.</span><span class="sxs-lookup"><span data-stu-id="b49fc-110">The application initially contains no packages.</span></span>

## <span data-ttu-id="b49fc-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="b49fc-111">PARAMETERS</span></span>

### <span data-ttu-id="b49fc-112">-Имя_учетной_записи</span><span class="sxs-lookup"><span data-stu-id="b49fc-112">-AccountName</span></span>
<span data-ttu-id="b49fc-113">Указывает имя пакетной учетной записи, к которой этот командлет добавляет приложение.</span><span class="sxs-lookup"><span data-stu-id="b49fc-113">Specifies the name of the Batch account to which this cmdlet adds an application.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b49fc-114">-AllowUpdates</span><span class="sxs-lookup"><span data-stu-id="b49fc-114">-AllowUpdates</span></span>
<span data-ttu-id="b49fc-115">Определяет, можно ли перезаписывать пакеты в приложении с использованием той же строки версии.</span><span class="sxs-lookup"><span data-stu-id="b49fc-115">Specifies whether packages within the application can be overwritten using the same version string.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b49fc-116">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="b49fc-116">-ApplicationId</span></span>
<span data-ttu-id="b49fc-117">Указывает идентификатор приложения.</span><span class="sxs-lookup"><span data-stu-id="b49fc-117">Specifies the ID of the application.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b49fc-118">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="b49fc-118">-DisplayName</span></span>
<span data-ttu-id="b49fc-119">Указывает отображаемое имя приложения.</span><span class="sxs-lookup"><span data-stu-id="b49fc-119">Specifies the display name for the application.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b49fc-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b49fc-120">-ResourceGroupName</span></span>
<span data-ttu-id="b49fc-121">Указывает имя группы ресурсов, которая содержит пакетную учетную запись.</span><span class="sxs-lookup"><span data-stu-id="b49fc-121">Specifies the name of the resource group that contains the Batch account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b49fc-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b49fc-122">-DefaultProfile</span></span>
<span data-ttu-id="b49fc-123">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="b49fc-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b49fc-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b49fc-124">CommonParameters</span></span>
<span data-ttu-id="b49fc-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="b49fc-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b49fc-126">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b49fc-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b49fc-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="b49fc-127">INPUTS</span></span>

## <span data-ttu-id="b49fc-128">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="b49fc-128">OUTPUTS</span></span>

### <span data-ttu-id="b49fc-129">Microsoft.Azure.Commands.BatCH. Models. PSApplication</span><span class="sxs-lookup"><span data-stu-id="b49fc-129">Microsoft.Azure.Commands.Batch.Models.PSApplication</span></span>

## <span data-ttu-id="b49fc-130">Пуск</span><span class="sxs-lookup"><span data-stu-id="b49fc-130">NOTES</span></span>

## <span data-ttu-id="b49fc-131">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b49fc-131">RELATED LINKS</span></span>

[<span data-ttu-id="b49fc-132">Get-AzureRmBatchApplication</span><span class="sxs-lookup"><span data-stu-id="b49fc-132">Get-AzureRmBatchApplication</span></span>](./Get-AzureRmBatchApplication.md)

[<span data-ttu-id="b49fc-133">Get-AzureRmBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="b49fc-133">Get-AzureRmBatchApplicationPackage</span></span>](./Get-AzureRmBatchApplicationPackage.md)

[<span data-ttu-id="b49fc-134">New-AzureRmBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="b49fc-134">New-AzureRmBatchApplicationPackage</span></span>](./New-AzureRmBatchApplicationPackage.md)

[<span data-ttu-id="b49fc-135">Remove-AzureRmBatchApplication</span><span class="sxs-lookup"><span data-stu-id="b49fc-135">Remove-AzureRmBatchApplication</span></span>](./Remove-AzureRmBatchApplication.md)

[<span data-ttu-id="b49fc-136">Remove-AzureRmBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="b49fc-136">Remove-AzureRmBatchApplicationPackage</span></span>](./Remove-AzureRmBatchApplicationPackage.md)

[<span data-ttu-id="b49fc-137">Set-AzureRmBatchApplication</span><span class="sxs-lookup"><span data-stu-id="b49fc-137">Set-AzureRmBatchApplication</span></span>](./Set-AzureRmBatchApplication.md)


