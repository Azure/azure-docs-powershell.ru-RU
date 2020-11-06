---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: FD2E3442-9CEA-4390-BE9C-772C7D6FD1E2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Remove-AzureRmBatchApplicationPackage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Remove-AzureRmBatchApplicationPackage.md
ms.openlocfilehash: 8ef7ba1c678c09ba10bd87c301a417600f51fe0c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93566309"
---
# <span data-ttu-id="b00e0-101">Remove-AzureRmBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="b00e0-101">Remove-AzureRmBatchApplicationPackage</span></span>

## <span data-ttu-id="b00e0-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="b00e0-102">SYNOPSIS</span></span>
<span data-ttu-id="b00e0-103">Удаляет запись пакета приложения и двоичный файл.</span><span class="sxs-lookup"><span data-stu-id="b00e0-103">Deletes an application package record and the binary file.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b00e0-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="b00e0-104">SYNTAX</span></span>

```
Remove-AzureRmBatchApplicationPackage [-AccountName] <String> [-ResourceGroupName] <String>
 [-ApplicationId] <String> [-ApplicationVersion] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="b00e0-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b00e0-105">DESCRIPTION</span></span>
<span data-ttu-id="b00e0-106">Командлет **Remove-AzureRmBatchApplicationPackage** удаляет запись пакета приложения и двоичный файл из пакетной учетной записи Azure.</span><span class="sxs-lookup"><span data-stu-id="b00e0-106">The **Remove-AzureRmBatchApplicationPackage** cmdlet deletes an application package record and the binary file from an Azure Batch account.</span></span>

## <span data-ttu-id="b00e0-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="b00e0-107">EXAMPLES</span></span>

### <span data-ttu-id="b00e0-108">Пример 1: Удаление пакета приложения из пакетной учетной записи</span><span class="sxs-lookup"><span data-stu-id="b00e0-108">Example 1: Delete an application package from a Batch account</span></span>
```
PS C:\>Remove-AzureRmBatchApplicationPackage -AccountName "ContosoBatch" -ResourceGroupName "ContosoBatchGroup" -ApplicationId "litware" -ApplicationVersion "1.0"
```

<span data-ttu-id="b00e0-109">Эта команда удаляет версию 1,0 приложения беседа Litware из учетной записи ContosoBatchGroup.</span><span class="sxs-lookup"><span data-stu-id="b00e0-109">This command deletes version 1.0 of the Litware application from the ContosoBatchGroup account.</span></span>
<span data-ttu-id="b00e0-110">Команда удаляет запись пакета и большой двоичный объект, который содержит двоичный файл пакета.</span><span class="sxs-lookup"><span data-stu-id="b00e0-110">The command deletes both the package record and the blob that contain the package binary file.</span></span>

## <span data-ttu-id="b00e0-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="b00e0-111">PARAMETERS</span></span>

### <span data-ttu-id="b00e0-112">-Имя_учетной_записи</span><span class="sxs-lookup"><span data-stu-id="b00e0-112">-AccountName</span></span>
<span data-ttu-id="b00e0-113">Указывает имя пакетной учетной записи, из которой этот командлет удаляет пакет приложения.</span><span class="sxs-lookup"><span data-stu-id="b00e0-113">Specifies the name of the Batch account from which this cmdlet deletes an application package.</span></span>

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

### <span data-ttu-id="b00e0-114">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="b00e0-114">-ApplicationId</span></span>
<span data-ttu-id="b00e0-115">Указывает идентификатор приложения.</span><span class="sxs-lookup"><span data-stu-id="b00e0-115">Specifies the ID of the application.</span></span>

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

### <span data-ttu-id="b00e0-116">-ApplicationVersion</span><span class="sxs-lookup"><span data-stu-id="b00e0-116">-ApplicationVersion</span></span>
<span data-ttu-id="b00e0-117">Определяет версию приложения.</span><span class="sxs-lookup"><span data-stu-id="b00e0-117">Specifies the version of the application.</span></span>

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

### <span data-ttu-id="b00e0-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b00e0-118">-ResourceGroupName</span></span>
<span data-ttu-id="b00e0-119">Указывает имя группы ресурсов, которая содержит пакетную учетную запись.</span><span class="sxs-lookup"><span data-stu-id="b00e0-119">Specifies the name of the resource group that contains the Batch account.</span></span>

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

### <span data-ttu-id="b00e0-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b00e0-120">-DefaultProfile</span></span>
<span data-ttu-id="b00e0-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="b00e0-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b00e0-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b00e0-122">CommonParameters</span></span>
<span data-ttu-id="b00e0-123">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="b00e0-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b00e0-124">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b00e0-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b00e0-125">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="b00e0-125">INPUTS</span></span>

## <span data-ttu-id="b00e0-126">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="b00e0-126">OUTPUTS</span></span>

## <span data-ttu-id="b00e0-127">Пуск</span><span class="sxs-lookup"><span data-stu-id="b00e0-127">NOTES</span></span>

## <span data-ttu-id="b00e0-128">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b00e0-128">RELATED LINKS</span></span>

[<span data-ttu-id="b00e0-129">Get-AzureRmBatchApplication</span><span class="sxs-lookup"><span data-stu-id="b00e0-129">Get-AzureRmBatchApplication</span></span>](./Get-AzureRmBatchApplication.md)

[<span data-ttu-id="b00e0-130">Get-AzureRmBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="b00e0-130">Get-AzureRmBatchApplicationPackage</span></span>](./Get-AzureRmBatchApplicationPackage.md)

[<span data-ttu-id="b00e0-131">New-AzureRmBatchApplication</span><span class="sxs-lookup"><span data-stu-id="b00e0-131">New-AzureRmBatchApplication</span></span>](./New-AzureRmBatchApplication.md)

[<span data-ttu-id="b00e0-132">New-AzureRmBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="b00e0-132">New-AzureRmBatchApplicationPackage</span></span>](./New-AzureRmBatchApplicationPackage.md)

[<span data-ttu-id="b00e0-133">Remove-AzureRmBatchApplication</span><span class="sxs-lookup"><span data-stu-id="b00e0-133">Remove-AzureRmBatchApplication</span></span>](./Remove-AzureRmBatchApplication.md)

[<span data-ttu-id="b00e0-134">Set-AzureRmBatchApplication</span><span class="sxs-lookup"><span data-stu-id="b00e0-134">Set-AzureRmBatchApplication</span></span>](./Set-AzureRmBatchApplication.md)


