---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: DCA1FD7A-54AF-48B1-A245-BFA9C43ACA9B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/set-azurermbatchapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Set-AzureRmBatchApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Set-AzureRmBatchApplication.md
ms.openlocfilehash: 8ede896e6a49cee5305e7f9fd42f6dab130e7986
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93565907"
---
# <span data-ttu-id="01ac9-101">Set-AzureRmBatchApplication</span><span class="sxs-lookup"><span data-stu-id="01ac9-101">Set-AzureRmBatchApplication</span></span>

## <span data-ttu-id="01ac9-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="01ac9-102">SYNOPSIS</span></span>
<span data-ttu-id="01ac9-103">Обновляет параметры указанного приложения.</span><span class="sxs-lookup"><span data-stu-id="01ac9-103">Updates settings for the specified application.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="01ac9-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="01ac9-104">SYNTAX</span></span>

```
Set-AzureRmBatchApplication [-AccountName] <String> [-ResourceGroupName] <String> [-ApplicationId] <String>
 [[-DisplayName] <String>] [[-DefaultVersion] <String>] [[-AllowUpdates] <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="01ac9-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="01ac9-105">DESCRIPTION</span></span>
<span data-ttu-id="01ac9-106">Командлет **Set-AzureRmBatchApplication** изменяет параметры для указанного пакетного приложения Azure.</span><span class="sxs-lookup"><span data-stu-id="01ac9-106">The **Set-AzureRmBatchApplication** cmdlet modifies settings for the specified Azure Batch application.</span></span>

## <span data-ttu-id="01ac9-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="01ac9-107">EXAMPLES</span></span>

### <span data-ttu-id="01ac9-108">Пример 1: обновление приложения в пакетной учетной записи</span><span class="sxs-lookup"><span data-stu-id="01ac9-108">Example 1: Update an application in a Batch account</span></span>
```
PS C:\>Set-AzureRmBatchApplication -AccountName "ContosoBatch" -ResourceGroupName "ContosoBatchGroup" -ApplicationId "Litware" -AllowUpdates $False
```

<span data-ttu-id="01ac9-109">Эта команда изменяет, разрешено ли обновление для приложения Llitware в учетной записи ContosoBatch.</span><span class="sxs-lookup"><span data-stu-id="01ac9-109">This command changes whether the Llitware application in the ContosoBatch account allows updates.</span></span>
<span data-ttu-id="01ac9-110">Команда не изменяет версию по умолчанию или отображаемое имя приложения.</span><span class="sxs-lookup"><span data-stu-id="01ac9-110">The command does not change the default version or display name of the application.</span></span>

## <span data-ttu-id="01ac9-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="01ac9-111">PARAMETERS</span></span>

### <span data-ttu-id="01ac9-112">-Имя_учетной_записи</span><span class="sxs-lookup"><span data-stu-id="01ac9-112">-AccountName</span></span>
<span data-ttu-id="01ac9-113">Указывает имя пакетной учетной записи, для которой этот командлет изменяет приложение.</span><span class="sxs-lookup"><span data-stu-id="01ac9-113">Specifies the name of the Batch account for which this cmdlet modifies an application.</span></span>

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

### <span data-ttu-id="01ac9-114">-AllowUpdates</span><span class="sxs-lookup"><span data-stu-id="01ac9-114">-AllowUpdates</span></span>
<span data-ttu-id="01ac9-115">Определяет, можно ли перезаписывать пакеты в приложении с использованием той же строки версии.</span><span class="sxs-lookup"><span data-stu-id="01ac9-115">Specifies whether packages within the application can be overwritten using the same version string.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="01ac9-116">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="01ac9-116">-ApplicationId</span></span>
<span data-ttu-id="01ac9-117">Указывает идентификатор приложения.</span><span class="sxs-lookup"><span data-stu-id="01ac9-117">Specifies the ID of the application.</span></span>

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

### <span data-ttu-id="01ac9-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="01ac9-118">-DefaultProfile</span></span>
<span data-ttu-id="01ac9-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="01ac9-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="01ac9-120">-DefaultVersion</span><span class="sxs-lookup"><span data-stu-id="01ac9-120">-DefaultVersion</span></span>
<span data-ttu-id="01ac9-121">Указывает, какой пакет следует использовать, если клиент запрашивает приложение, но не указывает версию.</span><span class="sxs-lookup"><span data-stu-id="01ac9-121">Specifies which package to use if a client requests the application but does not specify a version.</span></span>

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

### <span data-ttu-id="01ac9-122">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="01ac9-122">-DisplayName</span></span>
<span data-ttu-id="01ac9-123">Указывает отображаемое имя приложения.</span><span class="sxs-lookup"><span data-stu-id="01ac9-123">Specifies the display name for the application.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="01ac9-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="01ac9-124">-ResourceGroupName</span></span>
<span data-ttu-id="01ac9-125">Указывает имя группы ресурсов, которая содержит пакетную учетную запись.</span><span class="sxs-lookup"><span data-stu-id="01ac9-125">Specifies the name of the resource group that contains the Batch account.</span></span>

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

### <span data-ttu-id="01ac9-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="01ac9-126">CommonParameters</span></span>
<span data-ttu-id="01ac9-127">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="01ac9-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="01ac9-128">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="01ac9-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="01ac9-129">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="01ac9-129">INPUTS</span></span>

### <span data-ttu-id="01ac9-130">System. String</span><span class="sxs-lookup"><span data-stu-id="01ac9-130">System.String</span></span>

### <span data-ttu-id="01ac9-131">System. Nullable "1 [[System. Boolean, mscorlib, Version = 4.0.0.0, Culture = Neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="01ac9-131">System.Nullable\`1[[System.Boolean, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="01ac9-132">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="01ac9-132">OUTPUTS</span></span>

### <span data-ttu-id="01ac9-133">System. void</span><span class="sxs-lookup"><span data-stu-id="01ac9-133">System.Void</span></span>

## <span data-ttu-id="01ac9-134">Пуск</span><span class="sxs-lookup"><span data-stu-id="01ac9-134">NOTES</span></span>

## <span data-ttu-id="01ac9-135">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="01ac9-135">RELATED LINKS</span></span>

[<span data-ttu-id="01ac9-136">Get-AzureRmBatchApplication</span><span class="sxs-lookup"><span data-stu-id="01ac9-136">Get-AzureRmBatchApplication</span></span>](./Get-AzureRmBatchApplication.md)

[<span data-ttu-id="01ac9-137">Get-AzureRmBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="01ac9-137">Get-AzureRmBatchApplicationPackage</span></span>](./Get-AzureRmBatchApplicationPackage.md)

[<span data-ttu-id="01ac9-138">New-AzureRmBatchApplication</span><span class="sxs-lookup"><span data-stu-id="01ac9-138">New-AzureRmBatchApplication</span></span>](./New-AzureRmBatchApplication.md)

[<span data-ttu-id="01ac9-139">New-AzureRmBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="01ac9-139">New-AzureRmBatchApplicationPackage</span></span>](./New-AzureRmBatchApplicationPackage.md)

[<span data-ttu-id="01ac9-140">Remove-AzureRmBatchApplication</span><span class="sxs-lookup"><span data-stu-id="01ac9-140">Remove-AzureRmBatchApplication</span></span>](./Remove-AzureRmBatchApplication.md)

[<span data-ttu-id="01ac9-141">Remove-AzureRmBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="01ac9-141">Remove-AzureRmBatchApplicationPackage</span></span>](./Remove-AzureRmBatchApplicationPackage.md)


