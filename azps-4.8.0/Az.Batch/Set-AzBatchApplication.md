---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: DCA1FD7A-54AF-48B1-A245-BFA9C43ACA9B
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/set-azbatchapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Set-AzBatchApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Set-AzBatchApplication.md
ms.openlocfilehash: 6d6c72702d03b3b2174c21c786fb373374cea739
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94079179"
---
# <span data-ttu-id="b5963-101">Set-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="b5963-101">Set-AzBatchApplication</span></span>

## <span data-ttu-id="b5963-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="b5963-102">SYNOPSIS</span></span>
<span data-ttu-id="b5963-103">Обновляет параметры указанного приложения.</span><span class="sxs-lookup"><span data-stu-id="b5963-103">Updates settings for the specified application.</span></span>

## <span data-ttu-id="b5963-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="b5963-104">SYNTAX</span></span>

```
Set-AzBatchApplication [-AccountName] <String> [-ResourceGroupName] <String> [-ApplicationName] <String>
 [[-DisplayName] <String>] [[-DefaultVersion] <String>] [[-AllowUpdates] <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b5963-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b5963-105">DESCRIPTION</span></span>
<span data-ttu-id="b5963-106">Командлет **Set-AzBatchApplication** изменяет параметры для указанного пакетного приложения Azure.</span><span class="sxs-lookup"><span data-stu-id="b5963-106">The **Set-AzBatchApplication** cmdlet modifies settings for the specified Azure Batch application.</span></span>

## <span data-ttu-id="b5963-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="b5963-107">EXAMPLES</span></span>

### <span data-ttu-id="b5963-108">Пример 1: обновление приложения в пакетной учетной записи</span><span class="sxs-lookup"><span data-stu-id="b5963-108">Example 1: Update an application in a Batch account</span></span>
```
PS C:\>Set-AzBatchApplication -AccountName "ContosoBatch" -ResourceGroupName "ContosoBatchGroup" -ApplicationName "Litware" -AllowUpdates $False
```

<span data-ttu-id="b5963-109">Эта команда изменяет, разрешено ли обновление для приложения беседа Litware в учетной записи ContosoBatch.</span><span class="sxs-lookup"><span data-stu-id="b5963-109">This command changes whether the Litware application in the ContosoBatch account allows updates.</span></span>
<span data-ttu-id="b5963-110">Команда не изменяет версию по умолчанию или отображаемое имя приложения.</span><span class="sxs-lookup"><span data-stu-id="b5963-110">The command does not change the default version or display name of the application.</span></span>

## <span data-ttu-id="b5963-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="b5963-111">PARAMETERS</span></span>

### <span data-ttu-id="b5963-112">-Имя_учетной_записи</span><span class="sxs-lookup"><span data-stu-id="b5963-112">-AccountName</span></span>
<span data-ttu-id="b5963-113">Указывает имя пакетной учетной записи, для которой этот командлет изменяет приложение.</span><span class="sxs-lookup"><span data-stu-id="b5963-113">Specifies the name of the Batch account for which this cmdlet modifies an application.</span></span>

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

### <span data-ttu-id="b5963-114">-AllowUpdates</span><span class="sxs-lookup"><span data-stu-id="b5963-114">-AllowUpdates</span></span>
<span data-ttu-id="b5963-115">Определяет, можно ли перезаписывать пакеты в приложении с использованием той же строки версии.</span><span class="sxs-lookup"><span data-stu-id="b5963-115">Specifies whether packages within the application can be overwritten using the same version string.</span></span>

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

### <span data-ttu-id="b5963-116">-ИмяПриложения</span><span class="sxs-lookup"><span data-stu-id="b5963-116">-ApplicationName</span></span>
<span data-ttu-id="b5963-117">Указывает имя приложения.</span><span class="sxs-lookup"><span data-stu-id="b5963-117">Specifies the name of the application.</span></span>

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

### <span data-ttu-id="b5963-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b5963-118">-DefaultProfile</span></span>
<span data-ttu-id="b5963-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="b5963-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b5963-120">-DefaultVersion</span><span class="sxs-lookup"><span data-stu-id="b5963-120">-DefaultVersion</span></span>
<span data-ttu-id="b5963-121">Указывает, какой пакет следует использовать, если клиент запрашивает приложение, но не указывает версию.</span><span class="sxs-lookup"><span data-stu-id="b5963-121">Specifies which package to use if a client requests the application but does not specify a version.</span></span>

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

### <span data-ttu-id="b5963-122">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="b5963-122">-DisplayName</span></span>
<span data-ttu-id="b5963-123">Указывает отображаемое имя приложения.</span><span class="sxs-lookup"><span data-stu-id="b5963-123">Specifies the display name for the application.</span></span>

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

### <span data-ttu-id="b5963-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b5963-124">-ResourceGroupName</span></span>
<span data-ttu-id="b5963-125">Указывает имя группы ресурсов, которая содержит пакетную учетную запись.</span><span class="sxs-lookup"><span data-stu-id="b5963-125">Specifies the name of the resource group that contains the Batch account.</span></span>

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

### <span data-ttu-id="b5963-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b5963-126">CommonParameters</span></span>
<span data-ttu-id="b5963-127">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="b5963-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b5963-128">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b5963-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b5963-129">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="b5963-129">INPUTS</span></span>

### <span data-ttu-id="b5963-130">System. String</span><span class="sxs-lookup"><span data-stu-id="b5963-130">System.String</span></span>

### <span data-ttu-id="b5963-131">System. Nullable "1 [[System. Boolean, mscorlib, Version = 4.0.0.0, Culture = Neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="b5963-131">System.Nullable\`1[[System.Boolean, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="b5963-132">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="b5963-132">OUTPUTS</span></span>

### <span data-ttu-id="b5963-133">System. void</span><span class="sxs-lookup"><span data-stu-id="b5963-133">System.Void</span></span>

## <span data-ttu-id="b5963-134">Пуск</span><span class="sxs-lookup"><span data-stu-id="b5963-134">NOTES</span></span>

## <span data-ttu-id="b5963-135">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b5963-135">RELATED LINKS</span></span>

[<span data-ttu-id="b5963-136">Get-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="b5963-136">Get-AzBatchApplication</span></span>](./Get-AzBatchApplication.md)

[<span data-ttu-id="b5963-137">Get-AzBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="b5963-137">Get-AzBatchApplicationPackage</span></span>](./Get-AzBatchApplicationPackage.md)

[<span data-ttu-id="b5963-138">New-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="b5963-138">New-AzBatchApplication</span></span>](./New-AzBatchApplication.md)

[<span data-ttu-id="b5963-139">New-AzBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="b5963-139">New-AzBatchApplicationPackage</span></span>](./New-AzBatchApplicationPackage.md)

[<span data-ttu-id="b5963-140">Remove-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="b5963-140">Remove-AzBatchApplication</span></span>](./Remove-AzBatchApplication.md)

[<span data-ttu-id="b5963-141">Remove-AzBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="b5963-141">Remove-AzBatchApplicationPackage</span></span>](./Remove-AzBatchApplicationPackage.md)


