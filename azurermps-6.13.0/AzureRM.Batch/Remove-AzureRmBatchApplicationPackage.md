---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: FD2E3442-9CEA-4390-BE9C-772C7D6FD1E2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/remove-azurermbatchapplicationpackage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Remove-AzureRmBatchApplicationPackage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Remove-AzureRmBatchApplicationPackage.md
ms.openlocfilehash: 7d8552ccc2c293f33c71402043a28bfad32ceeeb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93558523"
---
# <span data-ttu-id="54b2e-101">Remove-AzureRmBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="54b2e-101">Remove-AzureRmBatchApplicationPackage</span></span>

## <span data-ttu-id="54b2e-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="54b2e-102">SYNOPSIS</span></span>
<span data-ttu-id="54b2e-103">Удаляет запись пакета приложения и двоичный файл.</span><span class="sxs-lookup"><span data-stu-id="54b2e-103">Deletes an application package record and the binary file.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="54b2e-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="54b2e-104">SYNTAX</span></span>

```
Remove-AzureRmBatchApplicationPackage [-AccountName] <String> [-ResourceGroupName] <String>
 [-ApplicationId] <String> [-ApplicationVersion] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="54b2e-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="54b2e-105">DESCRIPTION</span></span>
<span data-ttu-id="54b2e-106">Командлет **Remove-AzureRmBatchApplicationPackage** удаляет запись пакета приложения и двоичный файл из пакетной учетной записи Azure.</span><span class="sxs-lookup"><span data-stu-id="54b2e-106">The **Remove-AzureRmBatchApplicationPackage** cmdlet deletes an application package record and the binary file from an Azure Batch account.</span></span>

## <span data-ttu-id="54b2e-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="54b2e-107">EXAMPLES</span></span>

### <span data-ttu-id="54b2e-108">Пример 1: Удаление пакета приложения из пакетной учетной записи</span><span class="sxs-lookup"><span data-stu-id="54b2e-108">Example 1: Delete an application package from a Batch account</span></span>
```
PS C:\>Remove-AzureRmBatchApplicationPackage -AccountName "ContosoBatch" -ResourceGroupName "ContosoBatchGroup" -ApplicationId "litware" -ApplicationVersion "1.0"
```

<span data-ttu-id="54b2e-109">Эта команда удаляет версию 1,0 приложения беседа Litware из учетной записи ContosoBatchGroup.</span><span class="sxs-lookup"><span data-stu-id="54b2e-109">This command deletes version 1.0 of the Litware application from the ContosoBatchGroup account.</span></span>
<span data-ttu-id="54b2e-110">Команда удаляет запись пакета и большой двоичный объект, который содержит двоичный файл пакета.</span><span class="sxs-lookup"><span data-stu-id="54b2e-110">The command deletes both the package record and the blob that contain the package binary file.</span></span>

## <span data-ttu-id="54b2e-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="54b2e-111">PARAMETERS</span></span>

### <span data-ttu-id="54b2e-112">-Имя_учетной_записи</span><span class="sxs-lookup"><span data-stu-id="54b2e-112">-AccountName</span></span>
<span data-ttu-id="54b2e-113">Указывает имя пакетной учетной записи, из которой этот командлет удаляет пакет приложения.</span><span class="sxs-lookup"><span data-stu-id="54b2e-113">Specifies the name of the Batch account from which this cmdlet deletes an application package.</span></span>

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

### <span data-ttu-id="54b2e-114">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="54b2e-114">-ApplicationId</span></span>
<span data-ttu-id="54b2e-115">Указывает идентификатор приложения.</span><span class="sxs-lookup"><span data-stu-id="54b2e-115">Specifies the ID of the application.</span></span>

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

### <span data-ttu-id="54b2e-116">-ApplicationVersion</span><span class="sxs-lookup"><span data-stu-id="54b2e-116">-ApplicationVersion</span></span>
<span data-ttu-id="54b2e-117">Определяет версию приложения.</span><span class="sxs-lookup"><span data-stu-id="54b2e-117">Specifies the version of the application.</span></span>

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

### <span data-ttu-id="54b2e-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="54b2e-118">-DefaultProfile</span></span>
<span data-ttu-id="54b2e-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="54b2e-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="54b2e-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="54b2e-120">-ResourceGroupName</span></span>
<span data-ttu-id="54b2e-121">Указывает имя группы ресурсов, которая содержит пакетную учетную запись.</span><span class="sxs-lookup"><span data-stu-id="54b2e-121">Specifies the name of the resource group that contains the Batch account.</span></span>

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

### <span data-ttu-id="54b2e-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="54b2e-122">CommonParameters</span></span>
<span data-ttu-id="54b2e-123">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="54b2e-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="54b2e-124">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="54b2e-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="54b2e-125">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="54b2e-125">INPUTS</span></span>

### <span data-ttu-id="54b2e-126">System. String</span><span class="sxs-lookup"><span data-stu-id="54b2e-126">System.String</span></span>

## <span data-ttu-id="54b2e-127">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="54b2e-127">OUTPUTS</span></span>

### <span data-ttu-id="54b2e-128">System. void</span><span class="sxs-lookup"><span data-stu-id="54b2e-128">System.Void</span></span>

## <span data-ttu-id="54b2e-129">Пуск</span><span class="sxs-lookup"><span data-stu-id="54b2e-129">NOTES</span></span>

## <span data-ttu-id="54b2e-130">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="54b2e-130">RELATED LINKS</span></span>

[<span data-ttu-id="54b2e-131">Get-AzureRmBatchApplication</span><span class="sxs-lookup"><span data-stu-id="54b2e-131">Get-AzureRmBatchApplication</span></span>](./Get-AzureRmBatchApplication.md)

[<span data-ttu-id="54b2e-132">Get-AzureRmBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="54b2e-132">Get-AzureRmBatchApplicationPackage</span></span>](./Get-AzureRmBatchApplicationPackage.md)

[<span data-ttu-id="54b2e-133">New-AzureRmBatchApplication</span><span class="sxs-lookup"><span data-stu-id="54b2e-133">New-AzureRmBatchApplication</span></span>](./New-AzureRmBatchApplication.md)

[<span data-ttu-id="54b2e-134">New-AzureRmBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="54b2e-134">New-AzureRmBatchApplicationPackage</span></span>](./New-AzureRmBatchApplicationPackage.md)

[<span data-ttu-id="54b2e-135">Remove-AzureRmBatchApplication</span><span class="sxs-lookup"><span data-stu-id="54b2e-135">Remove-AzureRmBatchApplication</span></span>](./Remove-AzureRmBatchApplication.md)

[<span data-ttu-id="54b2e-136">Set-AzureRmBatchApplication</span><span class="sxs-lookup"><span data-stu-id="54b2e-136">Set-AzureRmBatchApplication</span></span>](./Set-AzureRmBatchApplication.md)


