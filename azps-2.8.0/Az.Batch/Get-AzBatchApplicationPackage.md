---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 17653793-3CE1-465F-87F7-20B4B8F56193
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/get-azbatchapplicationpackage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchApplicationPackage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchApplicationPackage.md
ms.openlocfilehash: 0cbcc49f4b37b150b783467f45dcc7d4d7e53f2c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93727704"
---
# <span data-ttu-id="238ad-101">Get-AzBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="238ad-101">Get-AzBatchApplicationPackage</span></span>

## <span data-ttu-id="238ad-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="238ad-102">SYNOPSIS</span></span>
<span data-ttu-id="238ad-103">Получает сведения о пакете приложения в пакетной учетной записи.</span><span class="sxs-lookup"><span data-stu-id="238ad-103">Gets information about an application package in a Batch account.</span></span>

## <span data-ttu-id="238ad-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="238ad-104">SYNTAX</span></span>

```
Get-AzBatchApplicationPackage [-AccountName] <String> [-ResourceGroupName] <String> [-ApplicationId] <String>
 [-ApplicationVersion] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="238ad-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="238ad-105">DESCRIPTION</span></span>
<span data-ttu-id="238ad-106">Командлет **Get-AzBatchApplicationPackage** получает сведения о пакете приложения в пакетной учетной записи Azure.</span><span class="sxs-lookup"><span data-stu-id="238ad-106">The **Get-AzBatchApplicationPackage** cmdlet gets information about an application package in an Azure Batch account.</span></span>

## <span data-ttu-id="238ad-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="238ad-107">EXAMPLES</span></span>

### <span data-ttu-id="238ad-108">Пример 1: получение сведений о пакете приложения в пакетной учетной записи</span><span class="sxs-lookup"><span data-stu-id="238ad-108">Example 1: Get details of an application package in a Batch account</span></span>
```
PS C:\>Get-AzBatchApplicationPackage -AccountName "ContosoBatch" -ResourceGroupName "ContosoBatchGroup" -ApplicationId "Litware" -ApplicationVersion "1.0"
Format             : zip
State              : Active
Version            : 1.0
LastActivationTime : 13/05/2016 4:03:24 AM
StorageUrl         : https://contosobatch.blob.core.windows.net/app-test
StorageUrlExpiry   : 13/05/2016 8:04:44 AM
Id                 : litware
```

<span data-ttu-id="238ad-109">Эта команда получает сведения о пакете беседа Litware версии 1,0.</span><span class="sxs-lookup"><span data-stu-id="238ad-109">This command gets the details of version 1.0 of the Litware package.</span></span>

## <span data-ttu-id="238ad-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="238ad-110">PARAMETERS</span></span>

### <span data-ttu-id="238ad-111">-Имя_учетной_записи</span><span class="sxs-lookup"><span data-stu-id="238ad-111">-AccountName</span></span>
<span data-ttu-id="238ad-112">Указывает имя пакетной учетной записи, из которой этот командлет получает сведения.</span><span class="sxs-lookup"><span data-stu-id="238ad-112">Specifies the name of the Batch account from which this cmdlet gets information.</span></span>

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

### <span data-ttu-id="238ad-113">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="238ad-113">-ApplicationId</span></span>
<span data-ttu-id="238ad-114">Указывает идентификатор приложения.</span><span class="sxs-lookup"><span data-stu-id="238ad-114">Specifies the ID of the application.</span></span>

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

### <span data-ttu-id="238ad-115">-ApplicationVersion</span><span class="sxs-lookup"><span data-stu-id="238ad-115">-ApplicationVersion</span></span>
<span data-ttu-id="238ad-116">Определяет версию приложения.</span><span class="sxs-lookup"><span data-stu-id="238ad-116">Specifies the version of the application.</span></span>

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

### <span data-ttu-id="238ad-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="238ad-117">-DefaultProfile</span></span>
<span data-ttu-id="238ad-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="238ad-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="238ad-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="238ad-119">-ResourceGroupName</span></span>
<span data-ttu-id="238ad-120">Указывает имя группы ресурсов, которая содержит пакетную учетную запись.</span><span class="sxs-lookup"><span data-stu-id="238ad-120">Specifies the name of the resource group that contains the Batch account.</span></span>

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

### <span data-ttu-id="238ad-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="238ad-121">CommonParameters</span></span>
<span data-ttu-id="238ad-122">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="238ad-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="238ad-123">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="238ad-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="238ad-124">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="238ad-124">INPUTS</span></span>

### <span data-ttu-id="238ad-125">System. String</span><span class="sxs-lookup"><span data-stu-id="238ad-125">System.String</span></span>

## <span data-ttu-id="238ad-126">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="238ad-126">OUTPUTS</span></span>

### <span data-ttu-id="238ad-127">Microsoft.Azure.Commands.BatCH. Models. PSApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="238ad-127">Microsoft.Azure.Commands.Batch.Models.PSApplicationPackage</span></span>

## <span data-ttu-id="238ad-128">Пуск</span><span class="sxs-lookup"><span data-stu-id="238ad-128">NOTES</span></span>

## <span data-ttu-id="238ad-129">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="238ad-129">RELATED LINKS</span></span>

[<span data-ttu-id="238ad-130">Get-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="238ad-130">Get-AzBatchApplication</span></span>](./Get-AzBatchApplication.md)

[<span data-ttu-id="238ad-131">New-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="238ad-131">New-AzBatchApplication</span></span>](./New-AzBatchApplication.md)

[<span data-ttu-id="238ad-132">New-AzBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="238ad-132">New-AzBatchApplicationPackage</span></span>](./New-AzBatchApplicationPackage.md)

[<span data-ttu-id="238ad-133">Remove-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="238ad-133">Remove-AzBatchApplication</span></span>](./Remove-AzBatchApplication.md)

[<span data-ttu-id="238ad-134">Remove-AzBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="238ad-134">Remove-AzBatchApplicationPackage</span></span>](./Remove-AzBatchApplicationPackage.md)

[<span data-ttu-id="238ad-135">Set-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="238ad-135">Set-AzBatchApplication</span></span>](./Set-AzBatchApplication.md)


