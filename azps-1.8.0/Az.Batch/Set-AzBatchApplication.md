---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: DCA1FD7A-54AF-48B1-A245-BFA9C43ACA9B
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/set-azbatchapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Set-AzBatchApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Set-AzBatchApplication.md
ms.openlocfilehash: 3dcbd81452ff9c4e5cf029b9c5d6169832d27a62
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93731454"
---
# <span data-ttu-id="1e843-101">Set-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="1e843-101">Set-AzBatchApplication</span></span>

## <span data-ttu-id="1e843-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="1e843-102">SYNOPSIS</span></span>
<span data-ttu-id="1e843-103">Обновляет параметры указанного приложения.</span><span class="sxs-lookup"><span data-stu-id="1e843-103">Updates settings for the specified application.</span></span>

## <span data-ttu-id="1e843-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="1e843-104">SYNTAX</span></span>

```
Set-AzBatchApplication [-AccountName] <String> [-ResourceGroupName] <String> [-ApplicationId] <String>
 [[-DisplayName] <String>] [[-DefaultVersion] <String>] [[-AllowUpdates] <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1e843-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="1e843-105">DESCRIPTION</span></span>
<span data-ttu-id="1e843-106">Командлет **Set-AzBatchApplication** изменяет параметры для указанного пакетного приложения Azure.</span><span class="sxs-lookup"><span data-stu-id="1e843-106">The **Set-AzBatchApplication** cmdlet modifies settings for the specified Azure Batch application.</span></span>

## <span data-ttu-id="1e843-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="1e843-107">EXAMPLES</span></span>

### <span data-ttu-id="1e843-108">Пример 1: обновление приложения в пакетной учетной записи</span><span class="sxs-lookup"><span data-stu-id="1e843-108">Example 1: Update an application in a Batch account</span></span>
```
PS C:\>Set-AzBatchApplication -AccountName "ContosoBatch" -ResourceGroupName "ContosoBatchGroup" -ApplicationId "Litware" -AllowUpdates $False
```

<span data-ttu-id="1e843-109">Эта команда изменяет, разрешено ли обновление для приложения Llitware в учетной записи ContosoBatch.</span><span class="sxs-lookup"><span data-stu-id="1e843-109">This command changes whether the Llitware application in the ContosoBatch account allows updates.</span></span>
<span data-ttu-id="1e843-110">Команда не изменяет версию по умолчанию или отображаемое имя приложения.</span><span class="sxs-lookup"><span data-stu-id="1e843-110">The command does not change the default version or display name of the application.</span></span>

## <span data-ttu-id="1e843-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="1e843-111">PARAMETERS</span></span>

### <span data-ttu-id="1e843-112">-Имя_учетной_записи</span><span class="sxs-lookup"><span data-stu-id="1e843-112">-AccountName</span></span>
<span data-ttu-id="1e843-113">Указывает имя пакетной учетной записи, для которой этот командлет изменяет приложение.</span><span class="sxs-lookup"><span data-stu-id="1e843-113">Specifies the name of the Batch account for which this cmdlet modifies an application.</span></span>

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

### <span data-ttu-id="1e843-114">-AllowUpdates</span><span class="sxs-lookup"><span data-stu-id="1e843-114">-AllowUpdates</span></span>
<span data-ttu-id="1e843-115">Определяет, можно ли перезаписывать пакеты в приложении с использованием той же строки версии.</span><span class="sxs-lookup"><span data-stu-id="1e843-115">Specifies whether packages within the application can be overwritten using the same version string.</span></span>

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

### <span data-ttu-id="1e843-116">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="1e843-116">-ApplicationId</span></span>
<span data-ttu-id="1e843-117">Указывает идентификатор приложения.</span><span class="sxs-lookup"><span data-stu-id="1e843-117">Specifies the ID of the application.</span></span>

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

### <span data-ttu-id="1e843-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1e843-118">-DefaultProfile</span></span>
<span data-ttu-id="1e843-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="1e843-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1e843-120">-DefaultVersion</span><span class="sxs-lookup"><span data-stu-id="1e843-120">-DefaultVersion</span></span>
<span data-ttu-id="1e843-121">Указывает, какой пакет следует использовать, если клиент запрашивает приложение, но не указывает версию.</span><span class="sxs-lookup"><span data-stu-id="1e843-121">Specifies which package to use if a client requests the application but does not specify a version.</span></span>

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

### <span data-ttu-id="1e843-122">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="1e843-122">-DisplayName</span></span>
<span data-ttu-id="1e843-123">Указывает отображаемое имя приложения.</span><span class="sxs-lookup"><span data-stu-id="1e843-123">Specifies the display name for the application.</span></span>

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

### <span data-ttu-id="1e843-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1e843-124">-ResourceGroupName</span></span>
<span data-ttu-id="1e843-125">Указывает имя группы ресурсов, которая содержит пакетную учетную запись.</span><span class="sxs-lookup"><span data-stu-id="1e843-125">Specifies the name of the resource group that contains the Batch account.</span></span>

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

### <span data-ttu-id="1e843-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1e843-126">CommonParameters</span></span>
<span data-ttu-id="1e843-127">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="1e843-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1e843-128">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1e843-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1e843-129">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="1e843-129">INPUTS</span></span>

### <span data-ttu-id="1e843-130">System. String</span><span class="sxs-lookup"><span data-stu-id="1e843-130">System.String</span></span>

### <span data-ttu-id="1e843-131">System. Nullable "1 [[System. Boolean, System. Private. CoreLib, Version = 4.0.0.0, культура = Neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="1e843-131">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="1e843-132">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="1e843-132">OUTPUTS</span></span>

### <span data-ttu-id="1e843-133">System. void</span><span class="sxs-lookup"><span data-stu-id="1e843-133">System.Void</span></span>

## <span data-ttu-id="1e843-134">Пуск</span><span class="sxs-lookup"><span data-stu-id="1e843-134">NOTES</span></span>

## <span data-ttu-id="1e843-135">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="1e843-135">RELATED LINKS</span></span>

[<span data-ttu-id="1e843-136">Get-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="1e843-136">Get-AzBatchApplication</span></span>](./Get-AzBatchApplication.md)

[<span data-ttu-id="1e843-137">Get-AzBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="1e843-137">Get-AzBatchApplicationPackage</span></span>](./Get-AzBatchApplicationPackage.md)

[<span data-ttu-id="1e843-138">New-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="1e843-138">New-AzBatchApplication</span></span>](./New-AzBatchApplication.md)

[<span data-ttu-id="1e843-139">New-AzBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="1e843-139">New-AzBatchApplicationPackage</span></span>](./New-AzBatchApplicationPackage.md)

[<span data-ttu-id="1e843-140">Remove-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="1e843-140">Remove-AzBatchApplication</span></span>](./Remove-AzBatchApplication.md)

[<span data-ttu-id="1e843-141">Remove-AzBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="1e843-141">Remove-AzBatchApplicationPackage</span></span>](./Remove-AzBatchApplicationPackage.md)


