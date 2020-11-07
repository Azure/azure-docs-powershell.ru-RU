---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: FD2E3442-9CEA-4390-BE9C-772C7D6FD1E2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/remove-azurermbatchapplicationpackage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Remove-AzureRmBatchApplicationPackage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Remove-AzureRmBatchApplicationPackage.md
ms.openlocfilehash: 0ae0003c4c38b7e3922694ed01f6d8f4d10a49d2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93734724"
---
# <span data-ttu-id="8d382-101">Remove-AzureRmBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="8d382-101">Remove-AzureRmBatchApplicationPackage</span></span>

## <span data-ttu-id="8d382-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="8d382-102">SYNOPSIS</span></span>
<span data-ttu-id="8d382-103">Удаляет запись пакета приложения и двоичный файл.</span><span class="sxs-lookup"><span data-stu-id="8d382-103">Deletes an application package record and the binary file.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8d382-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="8d382-104">SYNTAX</span></span>

```
Remove-AzureRmBatchApplicationPackage [-AccountName] <String> [-ResourceGroupName] <String>
 [-ApplicationId] <String> [-ApplicationVersion] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="8d382-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="8d382-105">DESCRIPTION</span></span>
<span data-ttu-id="8d382-106">Командлет **Remove-AzureRmBatchApplicationPackage** удаляет запись пакета приложения и двоичный файл из пакетной учетной записи Azure.</span><span class="sxs-lookup"><span data-stu-id="8d382-106">The **Remove-AzureRmBatchApplicationPackage** cmdlet deletes an application package record and the binary file from an Azure Batch account.</span></span>

## <span data-ttu-id="8d382-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="8d382-107">EXAMPLES</span></span>

### <span data-ttu-id="8d382-108">Пример 1: Удаление пакета приложения из пакетной учетной записи</span><span class="sxs-lookup"><span data-stu-id="8d382-108">Example 1: Delete an application package from a Batch account</span></span>
```
PS C:\>Remove-AzureRmBatchApplicationPackage -AccountName "ContosoBatch" -ResourceGroupName "ContosoBatchGroup" -ApplicationId "litware" -ApplicationVersion "1.0"
```

<span data-ttu-id="8d382-109">Эта команда удаляет версию 1,0 приложения беседа Litware из учетной записи ContosoBatchGroup.</span><span class="sxs-lookup"><span data-stu-id="8d382-109">This command deletes version 1.0 of the Litware application from the ContosoBatchGroup account.</span></span>
<span data-ttu-id="8d382-110">Команда удаляет запись пакета и большой двоичный объект, который содержит двоичный файл пакета.</span><span class="sxs-lookup"><span data-stu-id="8d382-110">The command deletes both the package record and the blob that contain the package binary file.</span></span>

## <span data-ttu-id="8d382-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="8d382-111">PARAMETERS</span></span>

### <span data-ttu-id="8d382-112">-Имя_учетной_записи</span><span class="sxs-lookup"><span data-stu-id="8d382-112">-AccountName</span></span>
<span data-ttu-id="8d382-113">Указывает имя пакетной учетной записи, из которой этот командлет удаляет пакет приложения.</span><span class="sxs-lookup"><span data-stu-id="8d382-113">Specifies the name of the Batch account from which this cmdlet deletes an application package.</span></span>

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

### <span data-ttu-id="8d382-114">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="8d382-114">-ApplicationId</span></span>
<span data-ttu-id="8d382-115">Указывает идентификатор приложения.</span><span class="sxs-lookup"><span data-stu-id="8d382-115">Specifies the ID of the application.</span></span>

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

### <span data-ttu-id="8d382-116">-ApplicationVersion</span><span class="sxs-lookup"><span data-stu-id="8d382-116">-ApplicationVersion</span></span>
<span data-ttu-id="8d382-117">Определяет версию приложения.</span><span class="sxs-lookup"><span data-stu-id="8d382-117">Specifies the version of the application.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8d382-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8d382-118">-DefaultProfile</span></span>
<span data-ttu-id="8d382-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="8d382-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8d382-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8d382-120">-ResourceGroupName</span></span>
<span data-ttu-id="8d382-121">Указывает имя группы ресурсов, которая содержит пакетную учетную запись.</span><span class="sxs-lookup"><span data-stu-id="8d382-121">Specifies the name of the resource group that contains the Batch account.</span></span>

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

### <span data-ttu-id="8d382-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8d382-122">CommonParameters</span></span>
<span data-ttu-id="8d382-123">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="8d382-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8d382-124">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8d382-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8d382-125">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="8d382-125">INPUTS</span></span>

### <span data-ttu-id="8d382-126">Ничего</span><span class="sxs-lookup"><span data-stu-id="8d382-126">None</span></span>
<span data-ttu-id="8d382-127">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="8d382-127">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="8d382-128">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="8d382-128">OUTPUTS</span></span>

## <span data-ttu-id="8d382-129">Пуск</span><span class="sxs-lookup"><span data-stu-id="8d382-129">NOTES</span></span>

## <span data-ttu-id="8d382-130">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="8d382-130">RELATED LINKS</span></span>

[<span data-ttu-id="8d382-131">Get-AzureRmBatchApplication</span><span class="sxs-lookup"><span data-stu-id="8d382-131">Get-AzureRmBatchApplication</span></span>](./Get-AzureRmBatchApplication.md)

[<span data-ttu-id="8d382-132">Get-AzureRmBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="8d382-132">Get-AzureRmBatchApplicationPackage</span></span>](./Get-AzureRmBatchApplicationPackage.md)

[<span data-ttu-id="8d382-133">New-AzureRmBatchApplication</span><span class="sxs-lookup"><span data-stu-id="8d382-133">New-AzureRmBatchApplication</span></span>](./New-AzureRmBatchApplication.md)

[<span data-ttu-id="8d382-134">New-AzureRmBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="8d382-134">New-AzureRmBatchApplicationPackage</span></span>](./New-AzureRmBatchApplicationPackage.md)

[<span data-ttu-id="8d382-135">Remove-AzureRmBatchApplication</span><span class="sxs-lookup"><span data-stu-id="8d382-135">Remove-AzureRmBatchApplication</span></span>](./Remove-AzureRmBatchApplication.md)

[<span data-ttu-id="8d382-136">Set-AzureRmBatchApplication</span><span class="sxs-lookup"><span data-stu-id="8d382-136">Set-AzureRmBatchApplication</span></span>](./Set-AzureRmBatchApplication.md)


