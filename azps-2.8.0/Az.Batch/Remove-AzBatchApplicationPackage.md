---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: FD2E3442-9CEA-4390-BE9C-772C7D6FD1E2
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/remove-azbatchapplicationpackage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Remove-AzBatchApplicationPackage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Remove-AzBatchApplicationPackage.md
ms.openlocfilehash: f4b47bb2abab783e4a6995ce57512dbd579e25e4
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93727690"
---
# <span data-ttu-id="67777-101">Remove-AzBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="67777-101">Remove-AzBatchApplicationPackage</span></span>

## <span data-ttu-id="67777-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="67777-102">SYNOPSIS</span></span>
<span data-ttu-id="67777-103">Удаляет запись пакета приложения и двоичный файл.</span><span class="sxs-lookup"><span data-stu-id="67777-103">Deletes an application package record and the binary file.</span></span>

## <span data-ttu-id="67777-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="67777-104">SYNTAX</span></span>

```
Remove-AzBatchApplicationPackage [-AccountName] <String> [-ResourceGroupName] <String>
 [-ApplicationId] <String> [-ApplicationVersion] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="67777-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="67777-105">DESCRIPTION</span></span>
<span data-ttu-id="67777-106">Командлет **Remove-AzBatchApplicationPackage** удаляет запись пакета приложения и двоичный файл из пакетной учетной записи Azure.</span><span class="sxs-lookup"><span data-stu-id="67777-106">The **Remove-AzBatchApplicationPackage** cmdlet deletes an application package record and the binary file from an Azure Batch account.</span></span>

## <span data-ttu-id="67777-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="67777-107">EXAMPLES</span></span>

### <span data-ttu-id="67777-108">Пример 1: Удаление пакета приложения из пакетной учетной записи</span><span class="sxs-lookup"><span data-stu-id="67777-108">Example 1: Delete an application package from a Batch account</span></span>
```
PS C:\>Remove-AzBatchApplicationPackage -AccountName "ContosoBatch" -ResourceGroupName "ContosoBatchGroup" -ApplicationId "litware" -ApplicationVersion "1.0"
```

<span data-ttu-id="67777-109">Эта команда удаляет версию 1,0 приложения беседа Litware из учетной записи ContosoBatchGroup.</span><span class="sxs-lookup"><span data-stu-id="67777-109">This command deletes version 1.0 of the Litware application from the ContosoBatchGroup account.</span></span>
<span data-ttu-id="67777-110">Команда удаляет запись пакета и большой двоичный объект, который содержит двоичный файл пакета.</span><span class="sxs-lookup"><span data-stu-id="67777-110">The command deletes both the package record and the blob that contain the package binary file.</span></span>

## <span data-ttu-id="67777-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="67777-111">PARAMETERS</span></span>

### <span data-ttu-id="67777-112">-Имя_учетной_записи</span><span class="sxs-lookup"><span data-stu-id="67777-112">-AccountName</span></span>
<span data-ttu-id="67777-113">Указывает имя пакетной учетной записи, из которой этот командлет удаляет пакет приложения.</span><span class="sxs-lookup"><span data-stu-id="67777-113">Specifies the name of the Batch account from which this cmdlet deletes an application package.</span></span>

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

### <span data-ttu-id="67777-114">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="67777-114">-ApplicationId</span></span>
<span data-ttu-id="67777-115">Указывает идентификатор приложения.</span><span class="sxs-lookup"><span data-stu-id="67777-115">Specifies the ID of the application.</span></span>

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

### <span data-ttu-id="67777-116">-ApplicationVersion</span><span class="sxs-lookup"><span data-stu-id="67777-116">-ApplicationVersion</span></span>
<span data-ttu-id="67777-117">Определяет версию приложения.</span><span class="sxs-lookup"><span data-stu-id="67777-117">Specifies the version of the application.</span></span>

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

### <span data-ttu-id="67777-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="67777-118">-DefaultProfile</span></span>
<span data-ttu-id="67777-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="67777-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="67777-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="67777-120">-ResourceGroupName</span></span>
<span data-ttu-id="67777-121">Указывает имя группы ресурсов, которая содержит пакетную учетную запись.</span><span class="sxs-lookup"><span data-stu-id="67777-121">Specifies the name of the resource group that contains the Batch account.</span></span>

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

### <span data-ttu-id="67777-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="67777-122">CommonParameters</span></span>
<span data-ttu-id="67777-123">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="67777-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="67777-124">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="67777-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="67777-125">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="67777-125">INPUTS</span></span>

### <span data-ttu-id="67777-126">System. String</span><span class="sxs-lookup"><span data-stu-id="67777-126">System.String</span></span>

## <span data-ttu-id="67777-127">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="67777-127">OUTPUTS</span></span>

### <span data-ttu-id="67777-128">System. void</span><span class="sxs-lookup"><span data-stu-id="67777-128">System.Void</span></span>

## <span data-ttu-id="67777-129">Пуск</span><span class="sxs-lookup"><span data-stu-id="67777-129">NOTES</span></span>

## <span data-ttu-id="67777-130">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="67777-130">RELATED LINKS</span></span>

[<span data-ttu-id="67777-131">Get-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="67777-131">Get-AzBatchApplication</span></span>](./Get-AzBatchApplication.md)

[<span data-ttu-id="67777-132">Get-AzBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="67777-132">Get-AzBatchApplicationPackage</span></span>](./Get-AzBatchApplicationPackage.md)

[<span data-ttu-id="67777-133">New-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="67777-133">New-AzBatchApplication</span></span>](./New-AzBatchApplication.md)

[<span data-ttu-id="67777-134">New-AzBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="67777-134">New-AzBatchApplicationPackage</span></span>](./New-AzBatchApplicationPackage.md)

[<span data-ttu-id="67777-135">Remove-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="67777-135">Remove-AzBatchApplication</span></span>](./Remove-AzBatchApplication.md)

[<span data-ttu-id="67777-136">Set-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="67777-136">Set-AzBatchApplication</span></span>](./Set-AzBatchApplication.md)


