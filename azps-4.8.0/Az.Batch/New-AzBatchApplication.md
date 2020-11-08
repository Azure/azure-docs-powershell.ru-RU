---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: FF111B74-90A3-4F7C-B515-CE1EEF68EB54
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/new-azbatchapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/New-AzBatchApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/New-AzBatchApplication.md
ms.openlocfilehash: 44d3c44effa74844713f6ecdf3012109f29b61b6
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94080069"
---
# <span data-ttu-id="15f47-101">New-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="15f47-101">New-AzBatchApplication</span></span>

## <span data-ttu-id="15f47-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="15f47-102">SYNOPSIS</span></span>
<span data-ttu-id="15f47-103">Добавляет приложение в указанную учетную запись пакета.</span><span class="sxs-lookup"><span data-stu-id="15f47-103">Adds an application to the specified Batch account.</span></span>

## <span data-ttu-id="15f47-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="15f47-104">SYNTAX</span></span>

```
New-AzBatchApplication [-AccountName] <String> [-ResourceGroupName] <String> [-ApplicationName] <String>
 [[-AllowUpdates] <Boolean>] [[-DisplayName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="15f47-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="15f47-105">DESCRIPTION</span></span>
<span data-ttu-id="15f47-106">Командлет **New-AzBatchApplication** добавляет приложение в указанную учетную запись пакета Azure.</span><span class="sxs-lookup"><span data-stu-id="15f47-106">The **New-AzBatchApplication** cmdlet adds an application to the specified Azure Batch account.</span></span>

## <span data-ttu-id="15f47-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="15f47-107">EXAMPLES</span></span>

### <span data-ttu-id="15f47-108">Пример 1: Добавление пустого приложения в пакетную учетную запись</span><span class="sxs-lookup"><span data-stu-id="15f47-108">Example 1: Add an empty application to a Batch account</span></span>
```
PS C:\>New-AzBatchApplication -AccountName "ContosoBatch" -ResourceGroupName "ContosoBatchGroup" -ApplicationName "Litware" -AllowUpdates $True -DisplayName "Litware Advanced Reticulator"
```

<span data-ttu-id="15f47-109">Эта команда создает приложение беседа Litware в учетной записи ContosoBatch.</span><span class="sxs-lookup"><span data-stu-id="15f47-109">This command creates the Litware application in the ContosoBatch account.</span></span>
<span data-ttu-id="15f47-110">Приложение изначально не включает пакеты.</span><span class="sxs-lookup"><span data-stu-id="15f47-110">The application initially contains no packages.</span></span>

## <span data-ttu-id="15f47-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="15f47-111">PARAMETERS</span></span>

### <span data-ttu-id="15f47-112">-Имя_учетной_записи</span><span class="sxs-lookup"><span data-stu-id="15f47-112">-AccountName</span></span>
<span data-ttu-id="15f47-113">Указывает имя пакетной учетной записи, к которой этот командлет добавляет приложение.</span><span class="sxs-lookup"><span data-stu-id="15f47-113">Specifies the name of the Batch account to which this cmdlet adds an application.</span></span>

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

### <span data-ttu-id="15f47-114">-AllowUpdates</span><span class="sxs-lookup"><span data-stu-id="15f47-114">-AllowUpdates</span></span>
<span data-ttu-id="15f47-115">Определяет, можно ли перезаписывать пакеты в приложении с использованием той же строки версии.</span><span class="sxs-lookup"><span data-stu-id="15f47-115">Specifies whether packages within the application can be overwritten using the same version string.</span></span>

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

### <span data-ttu-id="15f47-116">-ИмяПриложения</span><span class="sxs-lookup"><span data-stu-id="15f47-116">-ApplicationName</span></span>
<span data-ttu-id="15f47-117">Указывает имя приложения.</span><span class="sxs-lookup"><span data-stu-id="15f47-117">Specifies the name of the application.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ApplicationId

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="15f47-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="15f47-118">-DefaultProfile</span></span>
<span data-ttu-id="15f47-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="15f47-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="15f47-120">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="15f47-120">-DisplayName</span></span>
<span data-ttu-id="15f47-121">Указывает отображаемое имя приложения.</span><span class="sxs-lookup"><span data-stu-id="15f47-121">Specifies the display name for the application.</span></span>

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

### <span data-ttu-id="15f47-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="15f47-122">-ResourceGroupName</span></span>
<span data-ttu-id="15f47-123">Указывает имя группы ресурсов, которая содержит пакетную учетную запись.</span><span class="sxs-lookup"><span data-stu-id="15f47-123">Specifies the name of the resource group that contains the Batch account.</span></span>

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

### <span data-ttu-id="15f47-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="15f47-124">CommonParameters</span></span>
<span data-ttu-id="15f47-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="15f47-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="15f47-126">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="15f47-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="15f47-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="15f47-127">INPUTS</span></span>

### <span data-ttu-id="15f47-128">System. String</span><span class="sxs-lookup"><span data-stu-id="15f47-128">System.String</span></span>

### <span data-ttu-id="15f47-129">System. Nullable "1 [[System. Boolean, mscorlib, Version = 4.0.0.0, Culture = Neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="15f47-129">System.Nullable\`1[[System.Boolean, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="15f47-130">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="15f47-130">OUTPUTS</span></span>

### <span data-ttu-id="15f47-131">Microsoft.Azure.Commands.BatCH. Models. PSApplication</span><span class="sxs-lookup"><span data-stu-id="15f47-131">Microsoft.Azure.Commands.Batch.Models.PSApplication</span></span>

## <span data-ttu-id="15f47-132">Пуск</span><span class="sxs-lookup"><span data-stu-id="15f47-132">NOTES</span></span>

## <span data-ttu-id="15f47-133">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="15f47-133">RELATED LINKS</span></span>

[<span data-ttu-id="15f47-134">Get-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="15f47-134">Get-AzBatchApplication</span></span>](./Get-AzBatchApplication.md)

[<span data-ttu-id="15f47-135">Get-AzBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="15f47-135">Get-AzBatchApplicationPackage</span></span>](./Get-AzBatchApplicationPackage.md)

[<span data-ttu-id="15f47-136">New-AzBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="15f47-136">New-AzBatchApplicationPackage</span></span>](./New-AzBatchApplicationPackage.md)

[<span data-ttu-id="15f47-137">Remove-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="15f47-137">Remove-AzBatchApplication</span></span>](./Remove-AzBatchApplication.md)

[<span data-ttu-id="15f47-138">Remove-AzBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="15f47-138">Remove-AzBatchApplicationPackage</span></span>](./Remove-AzBatchApplicationPackage.md)

[<span data-ttu-id="15f47-139">Set-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="15f47-139">Set-AzBatchApplication</span></span>](./Set-AzBatchApplication.md)


