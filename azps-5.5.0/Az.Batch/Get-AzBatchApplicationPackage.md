---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 17653793-3CE1-465F-87F7-20B4B8F56193
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/get-azbatchapplicationpackage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchApplicationPackage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchApplicationPackage.md
ms.openlocfilehash: e5e289679327b0376530f01f91310cf211465e48
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100239408"
---
# <span data-ttu-id="05cbf-101">Get-AzBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="05cbf-101">Get-AzBatchApplicationPackage</span></span>

## <span data-ttu-id="05cbf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="05cbf-102">SYNOPSIS</span></span>
<span data-ttu-id="05cbf-103">Сведения о пакете приложения в пакетной учетной записи.</span><span class="sxs-lookup"><span data-stu-id="05cbf-103">Gets information about an application package in a Batch account.</span></span>

## <span data-ttu-id="05cbf-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="05cbf-104">SYNTAX</span></span>

```
Get-AzBatchApplicationPackage [-AccountName] <String> [-ResourceGroupName] <String> [-ApplicationName] <String>
 [[-ApplicationVersion] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="05cbf-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="05cbf-105">DESCRIPTION</span></span>
<span data-ttu-id="05cbf-106">Чтобы получить сведения о пакете приложения в учетной записи Azure Batch, можно получить сведения о пакете **Get-AzBatchApplicationPackage.**</span><span class="sxs-lookup"><span data-stu-id="05cbf-106">The **Get-AzBatchApplicationPackage** cmdlet gets information about an application package in an Azure Batch account.</span></span>

## <span data-ttu-id="05cbf-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="05cbf-107">EXAMPLES</span></span>

### <span data-ttu-id="05cbf-108">Пример 1. Получение сведений о пакете приложения в учетной записи пакета</span><span class="sxs-lookup"><span data-stu-id="05cbf-108">Example 1: Get details of an application package in a Batch account</span></span>
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

<span data-ttu-id="05cbf-109">Эта команда получает сведения о версии 1.0 пакета Litware.</span><span class="sxs-lookup"><span data-stu-id="05cbf-109">This command gets the details of version 1.0 of the Litware package.</span></span>

## <span data-ttu-id="05cbf-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="05cbf-110">PARAMETERS</span></span>

### <span data-ttu-id="05cbf-111">-AccountName</span><span class="sxs-lookup"><span data-stu-id="05cbf-111">-AccountName</span></span>
<span data-ttu-id="05cbf-112">Имя учетной записи пакета, из которой этот cmdlet получает сведения.</span><span class="sxs-lookup"><span data-stu-id="05cbf-112">Specifies the name of the Batch account from which this cmdlet gets information.</span></span>

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

### <span data-ttu-id="05cbf-113">-ApplicationName</span><span class="sxs-lookup"><span data-stu-id="05cbf-113">-ApplicationName</span></span>
<span data-ttu-id="05cbf-114">Указывает имя приложения.</span><span class="sxs-lookup"><span data-stu-id="05cbf-114">Specifies the name of the application.</span></span>

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

### <span data-ttu-id="05cbf-115">-ApplicationVersion</span><span class="sxs-lookup"><span data-stu-id="05cbf-115">-ApplicationVersion</span></span>
<span data-ttu-id="05cbf-116">Определяет версию приложения.</span><span class="sxs-lookup"><span data-stu-id="05cbf-116">Specifies the version of the application.</span></span>

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

### <span data-ttu-id="05cbf-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="05cbf-117">-DefaultProfile</span></span>
<span data-ttu-id="05cbf-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="05cbf-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="05cbf-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="05cbf-119">-ResourceGroupName</span></span>
<span data-ttu-id="05cbf-120">Имя группы ресурсов, которая содержит учетную запись пакета.</span><span class="sxs-lookup"><span data-stu-id="05cbf-120">Specifies the name of the resource group that contains the Batch account.</span></span>

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

### <span data-ttu-id="05cbf-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="05cbf-121">CommonParameters</span></span>
<span data-ttu-id="05cbf-122">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="05cbf-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="05cbf-123">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="05cbf-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="05cbf-124">INPUTS</span><span class="sxs-lookup"><span data-stu-id="05cbf-124">INPUTS</span></span>

### <span data-ttu-id="05cbf-125">System.String</span><span class="sxs-lookup"><span data-stu-id="05cbf-125">System.String</span></span>

## <span data-ttu-id="05cbf-126">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="05cbf-126">OUTPUTS</span></span>

### <span data-ttu-id="05cbf-127">Microsoft.Azure.Commands.Batch. Models.PSApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="05cbf-127">Microsoft.Azure.Commands.Batch.Models.PSApplicationPackage</span></span>

## <span data-ttu-id="05cbf-128">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="05cbf-128">NOTES</span></span>

## <span data-ttu-id="05cbf-129">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="05cbf-129">RELATED LINKS</span></span>

[<span data-ttu-id="05cbf-130">Get-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="05cbf-130">Get-AzBatchApplication</span></span>](./Get-AzBatchApplication.md)

[<span data-ttu-id="05cbf-131">New-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="05cbf-131">New-AzBatchApplication</span></span>](./New-AzBatchApplication.md)

[<span data-ttu-id="05cbf-132">New-AzBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="05cbf-132">New-AzBatchApplicationPackage</span></span>](./New-AzBatchApplicationPackage.md)

[<span data-ttu-id="05cbf-133">Remove-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="05cbf-133">Remove-AzBatchApplication</span></span>](./Remove-AzBatchApplication.md)

[<span data-ttu-id="05cbf-134">Remove-AzBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="05cbf-134">Remove-AzBatchApplicationPackage</span></span>](./Remove-AzBatchApplicationPackage.md)

[<span data-ttu-id="05cbf-135">Set-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="05cbf-135">Set-AzBatchApplication</span></span>](./Set-AzBatchApplication.md)


