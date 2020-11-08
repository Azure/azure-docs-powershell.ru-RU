---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 17653793-3CE1-465F-87F7-20B4B8F56193
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/get-azbatchapplicationpackage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchApplicationPackage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchApplicationPackage.md
ms.openlocfilehash: e5e289679327b0376530f01f91310cf211465e48
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94243708"
---
# <span data-ttu-id="06594-101">Get-AzBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="06594-101">Get-AzBatchApplicationPackage</span></span>

## <span data-ttu-id="06594-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="06594-102">SYNOPSIS</span></span>
<span data-ttu-id="06594-103">Получает сведения о пакете приложения в пакетной учетной записи.</span><span class="sxs-lookup"><span data-stu-id="06594-103">Gets information about an application package in a Batch account.</span></span>

## <span data-ttu-id="06594-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="06594-104">SYNTAX</span></span>

```
Get-AzBatchApplicationPackage [-AccountName] <String> [-ResourceGroupName] <String> [-ApplicationName] <String>
 [[-ApplicationVersion] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="06594-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="06594-105">DESCRIPTION</span></span>
<span data-ttu-id="06594-106">Командлет **Get-AzBatchApplicationPackage** получает сведения о пакете приложения в пакетной учетной записи Azure.</span><span class="sxs-lookup"><span data-stu-id="06594-106">The **Get-AzBatchApplicationPackage** cmdlet gets information about an application package in an Azure Batch account.</span></span>

## <span data-ttu-id="06594-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="06594-107">EXAMPLES</span></span>

### <span data-ttu-id="06594-108">Пример 1: получение сведений о пакете приложения в пакетной учетной записи</span><span class="sxs-lookup"><span data-stu-id="06594-108">Example 1: Get details of an application package in a Batch account</span></span>
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

<span data-ttu-id="06594-109">Эта команда получает сведения о пакете беседа Litware версии 1,0.</span><span class="sxs-lookup"><span data-stu-id="06594-109">This command gets the details of version 1.0 of the Litware package.</span></span>

## <span data-ttu-id="06594-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="06594-110">PARAMETERS</span></span>

### <span data-ttu-id="06594-111">-Имя_учетной_записи</span><span class="sxs-lookup"><span data-stu-id="06594-111">-AccountName</span></span>
<span data-ttu-id="06594-112">Указывает имя пакетной учетной записи, из которой этот командлет получает сведения.</span><span class="sxs-lookup"><span data-stu-id="06594-112">Specifies the name of the Batch account from which this cmdlet gets information.</span></span>

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

### <span data-ttu-id="06594-113">-ИмяПриложения</span><span class="sxs-lookup"><span data-stu-id="06594-113">-ApplicationName</span></span>
<span data-ttu-id="06594-114">Указывает имя приложения.</span><span class="sxs-lookup"><span data-stu-id="06594-114">Specifies the name of the application.</span></span>

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

### <span data-ttu-id="06594-115">-ApplicationVersion</span><span class="sxs-lookup"><span data-stu-id="06594-115">-ApplicationVersion</span></span>
<span data-ttu-id="06594-116">Определяет версию приложения.</span><span class="sxs-lookup"><span data-stu-id="06594-116">Specifies the version of the application.</span></span>

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

### <span data-ttu-id="06594-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="06594-117">-DefaultProfile</span></span>
<span data-ttu-id="06594-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="06594-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="06594-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="06594-119">-ResourceGroupName</span></span>
<span data-ttu-id="06594-120">Указывает имя группы ресурсов, которая содержит пакетную учетную запись.</span><span class="sxs-lookup"><span data-stu-id="06594-120">Specifies the name of the resource group that contains the Batch account.</span></span>

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

### <span data-ttu-id="06594-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="06594-121">CommonParameters</span></span>
<span data-ttu-id="06594-122">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="06594-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="06594-123">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="06594-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="06594-124">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="06594-124">INPUTS</span></span>

### <span data-ttu-id="06594-125">System. String</span><span class="sxs-lookup"><span data-stu-id="06594-125">System.String</span></span>

## <span data-ttu-id="06594-126">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="06594-126">OUTPUTS</span></span>

### <span data-ttu-id="06594-127">Microsoft.Azure.Commands.BatCH. Models. PSApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="06594-127">Microsoft.Azure.Commands.Batch.Models.PSApplicationPackage</span></span>

## <span data-ttu-id="06594-128">Пуск</span><span class="sxs-lookup"><span data-stu-id="06594-128">NOTES</span></span>

## <span data-ttu-id="06594-129">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="06594-129">RELATED LINKS</span></span>

[<span data-ttu-id="06594-130">Get-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="06594-130">Get-AzBatchApplication</span></span>](./Get-AzBatchApplication.md)

[<span data-ttu-id="06594-131">New-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="06594-131">New-AzBatchApplication</span></span>](./New-AzBatchApplication.md)

[<span data-ttu-id="06594-132">New-AzBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="06594-132">New-AzBatchApplicationPackage</span></span>](./New-AzBatchApplicationPackage.md)

[<span data-ttu-id="06594-133">Remove-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="06594-133">Remove-AzBatchApplication</span></span>](./Remove-AzBatchApplication.md)

[<span data-ttu-id="06594-134">Remove-AzBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="06594-134">Remove-AzBatchApplicationPackage</span></span>](./Remove-AzBatchApplicationPackage.md)

[<span data-ttu-id="06594-135">Set-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="06594-135">Set-AzBatchApplication</span></span>](./Set-AzBatchApplication.md)


