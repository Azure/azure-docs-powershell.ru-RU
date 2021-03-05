---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 17653793-3CE1-465F-87F7-20B4B8F56193
online version: https://docs.microsoft.com/powershell/module/az.batch/get-azbatchapplicationpackage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchApplicationPackage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchApplicationPackage.md
ms.openlocfilehash: c35630a7eda5c2174c85a5a792a03bb08ec09c1d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101987034"
---
# <span data-ttu-id="68465-101">Get-AzBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="68465-101">Get-AzBatchApplicationPackage</span></span>

## <span data-ttu-id="68465-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="68465-102">SYNOPSIS</span></span>
<span data-ttu-id="68465-103">Сведения о пакете приложения в пакетной учетной записи.</span><span class="sxs-lookup"><span data-stu-id="68465-103">Gets information about an application package in a Batch account.</span></span>

## <span data-ttu-id="68465-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="68465-104">SYNTAX</span></span>

```
Get-AzBatchApplicationPackage [-AccountName] <String> [-ResourceGroupName] <String> [-ApplicationName] <String>
 [[-ApplicationVersion] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="68465-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="68465-105">DESCRIPTION</span></span>
<span data-ttu-id="68465-106">Чтобы получить сведения о пакете приложения в учетной записи Azure Batch, можно получить сведения о пакете **Get-AzBatchApplicationPackage.**</span><span class="sxs-lookup"><span data-stu-id="68465-106">The **Get-AzBatchApplicationPackage** cmdlet gets information about an application package in an Azure Batch account.</span></span>

## <span data-ttu-id="68465-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="68465-107">EXAMPLES</span></span>

### <span data-ttu-id="68465-108">Пример 1. Получение сведений о пакете приложения в учетной записи пакета</span><span class="sxs-lookup"><span data-stu-id="68465-108">Example 1: Get details of an application package in a Batch account</span></span>
```
PS C:\>Get-AzBatchApplicationPackage -AccountName "ContosoBatch" -ResourceGroupName "ContosoBatchGroup" -ApplicationName "Litware" -ApplicationVersion "1.0"
Format             : zip
State              : Active
Version            : 1.0
LastActivationTime : 13/05/2016 4:03:24 AM
StorageUrl         : https://contosobatch.blob.core.windows.net/app-test
StorageUrlExpiry   : 13/05/2016 8:04:44 AM
Id                 : litware
```

<span data-ttu-id="68465-109">Эта команда получает сведения о версии 1.0 пакета Litware.</span><span class="sxs-lookup"><span data-stu-id="68465-109">This command gets the details of version 1.0 of the Litware package.</span></span>

## <span data-ttu-id="68465-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="68465-110">PARAMETERS</span></span>

### <span data-ttu-id="68465-111">-AccountName</span><span class="sxs-lookup"><span data-stu-id="68465-111">-AccountName</span></span>
<span data-ttu-id="68465-112">Имя учетной записи пакета, из которой этот cmdlet получает сведения.</span><span class="sxs-lookup"><span data-stu-id="68465-112">Specifies the name of the Batch account from which this cmdlet gets information.</span></span>

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

### <span data-ttu-id="68465-113">-ApplicationName</span><span class="sxs-lookup"><span data-stu-id="68465-113">-ApplicationName</span></span>
<span data-ttu-id="68465-114">Указывает имя приложения.</span><span class="sxs-lookup"><span data-stu-id="68465-114">Specifies the name of the application.</span></span>

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

### <span data-ttu-id="68465-115">-ApplicationVersion</span><span class="sxs-lookup"><span data-stu-id="68465-115">-ApplicationVersion</span></span>
<span data-ttu-id="68465-116">Определяет версию приложения.</span><span class="sxs-lookup"><span data-stu-id="68465-116">Specifies the version of the application.</span></span>

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

### <span data-ttu-id="68465-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="68465-117">-DefaultProfile</span></span>
<span data-ttu-id="68465-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="68465-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="68465-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="68465-119">-ResourceGroupName</span></span>
<span data-ttu-id="68465-120">Имя группы ресурсов, которая содержит учетную запись пакета.</span><span class="sxs-lookup"><span data-stu-id="68465-120">Specifies the name of the resource group that contains the Batch account.</span></span>

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

### <span data-ttu-id="68465-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="68465-121">CommonParameters</span></span>
<span data-ttu-id="68465-122">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="68465-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="68465-123">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="68465-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="68465-124">INPUTS</span><span class="sxs-lookup"><span data-stu-id="68465-124">INPUTS</span></span>

### <span data-ttu-id="68465-125">System.String</span><span class="sxs-lookup"><span data-stu-id="68465-125">System.String</span></span>

## <span data-ttu-id="68465-126">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="68465-126">OUTPUTS</span></span>

### <span data-ttu-id="68465-127">Microsoft.Azure.Commands.Batch. Models.PSApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="68465-127">Microsoft.Azure.Commands.Batch.Models.PSApplicationPackage</span></span>

## <span data-ttu-id="68465-128">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="68465-128">NOTES</span></span>

## <span data-ttu-id="68465-129">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="68465-129">RELATED LINKS</span></span>

[<span data-ttu-id="68465-130">Get-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="68465-130">Get-AzBatchApplication</span></span>](./Get-AzBatchApplication.md)

[<span data-ttu-id="68465-131">New-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="68465-131">New-AzBatchApplication</span></span>](./New-AzBatchApplication.md)

[<span data-ttu-id="68465-132">New-AzBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="68465-132">New-AzBatchApplicationPackage</span></span>](./New-AzBatchApplicationPackage.md)

[<span data-ttu-id="68465-133">Remove-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="68465-133">Remove-AzBatchApplication</span></span>](./Remove-AzBatchApplication.md)

[<span data-ttu-id="68465-134">Remove-AzBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="68465-134">Remove-AzBatchApplicationPackage</span></span>](./Remove-AzBatchApplicationPackage.md)

[<span data-ttu-id="68465-135">Set-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="68465-135">Set-AzBatchApplication</span></span>](./Set-AzBatchApplication.md)


