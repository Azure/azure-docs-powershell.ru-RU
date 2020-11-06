---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 17653793-3CE1-465F-87F7-20B4B8F56193
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureRmBatchApplicationPackage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureRmBatchApplicationPackage.md
ms.openlocfilehash: f260af1bc26d9cf921a26e4f08c3c4feab4b79c2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93565269"
---
# <span data-ttu-id="ac3ed-101">Get-AzureRmBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="ac3ed-101">Get-AzureRmBatchApplicationPackage</span></span>

## <span data-ttu-id="ac3ed-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="ac3ed-102">SYNOPSIS</span></span>
<span data-ttu-id="ac3ed-103">Получает сведения о пакете приложения в пакетной учетной записи.</span><span class="sxs-lookup"><span data-stu-id="ac3ed-103">Gets information about an application package in a Batch account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ac3ed-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="ac3ed-104">SYNTAX</span></span>

```
Get-AzureRmBatchApplicationPackage [-AccountName] <String> [-ResourceGroupName] <String>
 [-ApplicationId] <String> [-ApplicationVersion] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="ac3ed-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ac3ed-105">DESCRIPTION</span></span>
<span data-ttu-id="ac3ed-106">Командлет **Get-AzureRmBatchApplicationPackage** получает сведения о пакете приложения в пакетной учетной записи Azure.</span><span class="sxs-lookup"><span data-stu-id="ac3ed-106">The **Get-AzureRmBatchApplicationPackage** cmdlet gets information about an application package in an Azure Batch account.</span></span>

## <span data-ttu-id="ac3ed-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="ac3ed-107">EXAMPLES</span></span>

### <span data-ttu-id="ac3ed-108">Пример 1: получение сведений о пакете приложения в пакетной учетной записи</span><span class="sxs-lookup"><span data-stu-id="ac3ed-108">Example 1: Get details of an application package in a Batch account</span></span>
```
PS C:\>Get-AzureRmBatchApplicationPackage -AccountName "ContosoBatch" -ResourceGroupName "ContosoBatchGroup" -ApplicationId "Litware" -ApplicationVersion "1.0"
Format             : zip
State              : Active
Version            : 1.0
LastActivationTime : 13/05/2016 4:03:24 AM
StorageUrl         : https://contosobatch.blob.core.windows.net/app-test
StorageUrlExpiry   : 13/05/2016 8:04:44 AM
Id                 : litware
```

<span data-ttu-id="ac3ed-109">Эта команда получает сведения о пакете беседа Litware версии 1,0.</span><span class="sxs-lookup"><span data-stu-id="ac3ed-109">This command gets the details of version 1.0 of the Litware package.</span></span>

## <span data-ttu-id="ac3ed-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="ac3ed-110">PARAMETERS</span></span>

### <span data-ttu-id="ac3ed-111">-Имя_учетной_записи</span><span class="sxs-lookup"><span data-stu-id="ac3ed-111">-AccountName</span></span>
<span data-ttu-id="ac3ed-112">Указывает имя пакетной учетной записи, из которой этот командлет получает сведения.</span><span class="sxs-lookup"><span data-stu-id="ac3ed-112">Specifies the name of the Batch account from which this cmdlet gets information.</span></span>

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

### <span data-ttu-id="ac3ed-113">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="ac3ed-113">-ApplicationId</span></span>
<span data-ttu-id="ac3ed-114">Указывает идентификатор приложения.</span><span class="sxs-lookup"><span data-stu-id="ac3ed-114">Specifies the ID of the application.</span></span>

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

### <span data-ttu-id="ac3ed-115">-ApplicationVersion</span><span class="sxs-lookup"><span data-stu-id="ac3ed-115">-ApplicationVersion</span></span>
<span data-ttu-id="ac3ed-116">Определяет версию приложения.</span><span class="sxs-lookup"><span data-stu-id="ac3ed-116">Specifies the version of the application.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ac3ed-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ac3ed-117">-ResourceGroupName</span></span>
<span data-ttu-id="ac3ed-118">Указывает имя группы ресурсов, которая содержит пакетную учетную запись.</span><span class="sxs-lookup"><span data-stu-id="ac3ed-118">Specifies the name of the resource group that contains the Batch account.</span></span>

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

### <span data-ttu-id="ac3ed-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ac3ed-119">-DefaultProfile</span></span>
<span data-ttu-id="ac3ed-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="ac3ed-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ac3ed-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ac3ed-121">CommonParameters</span></span>
<span data-ttu-id="ac3ed-122">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="ac3ed-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ac3ed-123">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ac3ed-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ac3ed-124">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="ac3ed-124">INPUTS</span></span>

## <span data-ttu-id="ac3ed-125">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="ac3ed-125">OUTPUTS</span></span>

### <span data-ttu-id="ac3ed-126">Microsoft.Azure.Commands.BatCH. Models. PSApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="ac3ed-126">Microsoft.Azure.Commands.Batch.Models.PSApplicationPackage</span></span>

## <span data-ttu-id="ac3ed-127">Пуск</span><span class="sxs-lookup"><span data-stu-id="ac3ed-127">NOTES</span></span>

## <span data-ttu-id="ac3ed-128">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ac3ed-128">RELATED LINKS</span></span>

[<span data-ttu-id="ac3ed-129">Get-AzureRmBatchApplication</span><span class="sxs-lookup"><span data-stu-id="ac3ed-129">Get-AzureRmBatchApplication</span></span>](./Get-AzureRmBatchApplication.md)

[<span data-ttu-id="ac3ed-130">New-AzureRmBatchApplication</span><span class="sxs-lookup"><span data-stu-id="ac3ed-130">New-AzureRmBatchApplication</span></span>](./New-AzureRmBatchApplication.md)

[<span data-ttu-id="ac3ed-131">New-AzureRmBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="ac3ed-131">New-AzureRmBatchApplicationPackage</span></span>](./New-AzureRmBatchApplicationPackage.md)

[<span data-ttu-id="ac3ed-132">Remove-AzureRmBatchApplication</span><span class="sxs-lookup"><span data-stu-id="ac3ed-132">Remove-AzureRmBatchApplication</span></span>](./Remove-AzureRmBatchApplication.md)

[<span data-ttu-id="ac3ed-133">Remove-AzureRmBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="ac3ed-133">Remove-AzureRmBatchApplicationPackage</span></span>](./Remove-AzureRmBatchApplicationPackage.md)

[<span data-ttu-id="ac3ed-134">Set-AzureRmBatchApplication</span><span class="sxs-lookup"><span data-stu-id="ac3ed-134">Set-AzureRmBatchApplication</span></span>](./Set-AzureRmBatchApplication.md)


