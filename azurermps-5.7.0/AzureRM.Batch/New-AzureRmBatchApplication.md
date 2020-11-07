---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: FF111B74-90A3-4F7C-B515-CE1EEF68EB54
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/new-azurermbatchapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/New-AzureRmBatchApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/New-AzureRmBatchApplication.md
ms.openlocfilehash: 77b3d446c52e72bc31a2802768b00822982d1ea2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93734185"
---
# <span data-ttu-id="2e8e8-101">New-AzureRmBatchApplication</span><span class="sxs-lookup"><span data-stu-id="2e8e8-101">New-AzureRmBatchApplication</span></span>

## <span data-ttu-id="2e8e8-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="2e8e8-102">SYNOPSIS</span></span>
<span data-ttu-id="2e8e8-103">Добавляет приложение в указанную учетную запись пакета.</span><span class="sxs-lookup"><span data-stu-id="2e8e8-103">Adds an application to the specified Batch account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2e8e8-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="2e8e8-104">SYNTAX</span></span>

```
New-AzureRmBatchApplication [-AccountName] <String> [-ResourceGroupName] <String> [-ApplicationId] <String>
 [[-AllowUpdates] <Boolean>] [[-DisplayName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="2e8e8-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="2e8e8-105">DESCRIPTION</span></span>
<span data-ttu-id="2e8e8-106">Командлет **New-AzureRmBatchApplication** добавляет приложение в указанную учетную запись пакета Azure.</span><span class="sxs-lookup"><span data-stu-id="2e8e8-106">The **New-AzureRmBatchApplication** cmdlet adds an application to the specified Azure Batch account.</span></span>

## <span data-ttu-id="2e8e8-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="2e8e8-107">EXAMPLES</span></span>

### <span data-ttu-id="2e8e8-108">Пример 1: Добавление пустого приложения в пакетную учетную запись</span><span class="sxs-lookup"><span data-stu-id="2e8e8-108">Example 1: Add an empty application to a Batch account</span></span>
```
PS C:\>New-AzureRmBatchApplication -AccountName "ContosoBatch" -ResourceGroupName "ContosoBatchGroup" -ApplicationId "Litware" -AllowUpdates $True -DisplayName "Litware Advanced Reticulator"
```

<span data-ttu-id="2e8e8-109">Эта команда создает приложение беседа Litware в учетной записи ContosoBatch.</span><span class="sxs-lookup"><span data-stu-id="2e8e8-109">This command creates the Litware application in the ContosoBatch account.</span></span>
<span data-ttu-id="2e8e8-110">Приложение изначально не включает пакеты.</span><span class="sxs-lookup"><span data-stu-id="2e8e8-110">The application initially contains no packages.</span></span>

## <span data-ttu-id="2e8e8-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="2e8e8-111">PARAMETERS</span></span>

### <span data-ttu-id="2e8e8-112">-Имя_учетной_записи</span><span class="sxs-lookup"><span data-stu-id="2e8e8-112">-AccountName</span></span>
<span data-ttu-id="2e8e8-113">Указывает имя пакетной учетной записи, к которой этот командлет добавляет приложение.</span><span class="sxs-lookup"><span data-stu-id="2e8e8-113">Specifies the name of the Batch account to which this cmdlet adds an application.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2e8e8-114">-AllowUpdates</span><span class="sxs-lookup"><span data-stu-id="2e8e8-114">-AllowUpdates</span></span>
<span data-ttu-id="2e8e8-115">Определяет, можно ли перезаписывать пакеты в приложении с использованием той же строки версии.</span><span class="sxs-lookup"><span data-stu-id="2e8e8-115">Specifies whether packages within the application can be overwritten using the same version string.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2e8e8-116">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="2e8e8-116">-ApplicationId</span></span>
<span data-ttu-id="2e8e8-117">Указывает идентификатор приложения.</span><span class="sxs-lookup"><span data-stu-id="2e8e8-117">Specifies the ID of the application.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2e8e8-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2e8e8-118">-DefaultProfile</span></span>
<span data-ttu-id="2e8e8-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="2e8e8-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2e8e8-120">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="2e8e8-120">-DisplayName</span></span>
<span data-ttu-id="2e8e8-121">Указывает отображаемое имя приложения.</span><span class="sxs-lookup"><span data-stu-id="2e8e8-121">Specifies the display name for the application.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2e8e8-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2e8e8-122">-ResourceGroupName</span></span>
<span data-ttu-id="2e8e8-123">Указывает имя группы ресурсов, которая содержит пакетную учетную запись.</span><span class="sxs-lookup"><span data-stu-id="2e8e8-123">Specifies the name of the resource group that contains the Batch account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2e8e8-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2e8e8-124">CommonParameters</span></span>
<span data-ttu-id="2e8e8-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="2e8e8-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2e8e8-126">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2e8e8-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2e8e8-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="2e8e8-127">INPUTS</span></span>

### <span data-ttu-id="2e8e8-128">Ничего</span><span class="sxs-lookup"><span data-stu-id="2e8e8-128">None</span></span>
<span data-ttu-id="2e8e8-129">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="2e8e8-129">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="2e8e8-130">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="2e8e8-130">OUTPUTS</span></span>

### <span data-ttu-id="2e8e8-131">Microsoft.Azure.Commands.BatCH. Models. PSApplication</span><span class="sxs-lookup"><span data-stu-id="2e8e8-131">Microsoft.Azure.Commands.Batch.Models.PSApplication</span></span>

## <span data-ttu-id="2e8e8-132">Пуск</span><span class="sxs-lookup"><span data-stu-id="2e8e8-132">NOTES</span></span>

## <span data-ttu-id="2e8e8-133">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="2e8e8-133">RELATED LINKS</span></span>

[<span data-ttu-id="2e8e8-134">Get-AzureRmBatchApplication</span><span class="sxs-lookup"><span data-stu-id="2e8e8-134">Get-AzureRmBatchApplication</span></span>](./Get-AzureRmBatchApplication.md)

[<span data-ttu-id="2e8e8-135">Get-AzureRmBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="2e8e8-135">Get-AzureRmBatchApplicationPackage</span></span>](./Get-AzureRmBatchApplicationPackage.md)

[<span data-ttu-id="2e8e8-136">New-AzureRmBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="2e8e8-136">New-AzureRmBatchApplicationPackage</span></span>](./New-AzureRmBatchApplicationPackage.md)

[<span data-ttu-id="2e8e8-137">Remove-AzureRmBatchApplication</span><span class="sxs-lookup"><span data-stu-id="2e8e8-137">Remove-AzureRmBatchApplication</span></span>](./Remove-AzureRmBatchApplication.md)

[<span data-ttu-id="2e8e8-138">Remove-AzureRmBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="2e8e8-138">Remove-AzureRmBatchApplicationPackage</span></span>](./Remove-AzureRmBatchApplicationPackage.md)

[<span data-ttu-id="2e8e8-139">Set-AzureRmBatchApplication</span><span class="sxs-lookup"><span data-stu-id="2e8e8-139">Set-AzureRmBatchApplication</span></span>](./Set-AzureRmBatchApplication.md)


