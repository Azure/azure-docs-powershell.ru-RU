---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: D53DAEB6-DC4F-473C-A193-A1E2A65326D4
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/new-azbatchapplicationpackage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/New-AzBatchApplicationPackage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/New-AzBatchApplicationPackage.md
ms.openlocfilehash: fc23c99cabe76834204f2fac1f3c18ae7eea1df0
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98509650"
---
# <span data-ttu-id="240e5-101">New-AzBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="240e5-101">New-AzBatchApplicationPackage</span></span>

## <span data-ttu-id="240e5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="240e5-102">SYNOPSIS</span></span>
<span data-ttu-id="240e5-103">Создает пакет приложения в пакетной учетной записи.</span><span class="sxs-lookup"><span data-stu-id="240e5-103">Creates an application package in a Batch account.</span></span>

## <span data-ttu-id="240e5-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="240e5-104">SYNTAX</span></span>

### <span data-ttu-id="240e5-105">UploadAndActivate (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="240e5-105">UploadAndActivate (Default)</span></span>
```
New-AzBatchApplicationPackage [-AccountName] <String> [-ResourceGroupName] <String> [-ApplicationName] <String>
 [-ApplicationVersion] <String> [-Format] <String> -FilePath <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="240e5-106">ActivateOnly</span><span class="sxs-lookup"><span data-stu-id="240e5-106">ActivateOnly</span></span>
```
New-AzBatchApplicationPackage [-AccountName] <String> [-ResourceGroupName] <String> [-ApplicationName] <String>
 [-ApplicationVersion] <String> [-Format] <String> [-ActivateOnly] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="240e5-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="240e5-107">DESCRIPTION</span></span>
<span data-ttu-id="240e5-108">**Новый-AzBatchApplicationPackage** создает пакет приложения в учетной записи Azure Batch.</span><span class="sxs-lookup"><span data-stu-id="240e5-108">The **New-AzBatchApplicationPackage** cmdlet creates an application package in an Azure Batch account.</span></span>

## <span data-ttu-id="240e5-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="240e5-109">EXAMPLES</span></span>

### <span data-ttu-id="240e5-110">Пример 1. Установка пакета приложения в пакетную учетную запись</span><span class="sxs-lookup"><span data-stu-id="240e5-110">Example 1: Install an application package into a Batch account</span></span>
```
PS C:\>New-AzBatchApplicationPackage -AccountName "ContosoBatch" -ResourceGroupName "ContosoBatchGroup" -ApplicationName "Litware" -ApplicationVersion "1.0" -FilePath "litware.1.0.zip" -Format "zip"
```

<span data-ttu-id="240e5-111">Эта команда создает и активирует версию 1.0 приложения Litware, а также передает содержимое litware.1.0.zip пакета приложения.</span><span class="sxs-lookup"><span data-stu-id="240e5-111">This command creates and activates version 1.0 of the Litware application, and uploads the contents of litware.1.0.zip as the application package content.</span></span>

## <span data-ttu-id="240e5-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="240e5-112">PARAMETERS</span></span>

### <span data-ttu-id="240e5-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="240e5-113">-AccountName</span></span>
<span data-ttu-id="240e5-114">Имя учетной записи пакета, в которую этот cmdlet добавляет пакет приложения.</span><span class="sxs-lookup"><span data-stu-id="240e5-114">Specifies the name of the Batch account to which this cmdlet adds an application package.</span></span>

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

### <span data-ttu-id="240e5-115">-ActivateOnly</span><span class="sxs-lookup"><span data-stu-id="240e5-115">-ActivateOnly</span></span>
<span data-ttu-id="240e5-116">Указывает на то, что этот cmdlet активирует пакет приложения, который уже был добавлен.</span><span class="sxs-lookup"><span data-stu-id="240e5-116">Indicates that this cmdlet activates an application package that has already been uploaded.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ActivateOnly
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="240e5-117">-ApplicationName</span><span class="sxs-lookup"><span data-stu-id="240e5-117">-ApplicationName</span></span>
<span data-ttu-id="240e5-118">Указывает имя приложения.</span><span class="sxs-lookup"><span data-stu-id="240e5-118">Specifies the name of the application.</span></span>

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

### <span data-ttu-id="240e5-119">-ApplicationVersion</span><span class="sxs-lookup"><span data-stu-id="240e5-119">-ApplicationVersion</span></span>
<span data-ttu-id="240e5-120">Определяет версию приложения.</span><span class="sxs-lookup"><span data-stu-id="240e5-120">Specifies the version of the application.</span></span>

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

### <span data-ttu-id="240e5-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="240e5-121">-DefaultProfile</span></span>
<span data-ttu-id="240e5-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="240e5-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="240e5-123">-FilePath</span><span class="sxs-lookup"><span data-stu-id="240e5-123">-FilePath</span></span>
<span data-ttu-id="240e5-124">Указывает, что файл будет добавлен как двоичный файл пакета приложения.</span><span class="sxs-lookup"><span data-stu-id="240e5-124">Specifies the file to be uploaded as the application package binary file.</span></span>

```yaml
Type: System.String
Parameter Sets: UploadAndActivate
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="240e5-125">-Format</span><span class="sxs-lookup"><span data-stu-id="240e5-125">-Format</span></span>
<span data-ttu-id="240e5-126">Формат двоичного файла пакета приложения.</span><span class="sxs-lookup"><span data-stu-id="240e5-126">Specifies the format of the application package binary file.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="240e5-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="240e5-127">-ResourceGroupName</span></span>
<span data-ttu-id="240e5-128">Имя группы ресурсов, которая содержит учетную запись пакета.</span><span class="sxs-lookup"><span data-stu-id="240e5-128">Specifies the name of the resource group that contains the Batch account.</span></span>

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

### <span data-ttu-id="240e5-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="240e5-129">CommonParameters</span></span>
<span data-ttu-id="240e5-130">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="240e5-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="240e5-131">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="240e5-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="240e5-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="240e5-132">INPUTS</span></span>

### <span data-ttu-id="240e5-133">System.String</span><span class="sxs-lookup"><span data-stu-id="240e5-133">System.String</span></span>

### <span data-ttu-id="240e5-134">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="240e5-134">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="240e5-135">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="240e5-135">OUTPUTS</span></span>

### <span data-ttu-id="240e5-136">Microsoft.Azure.Commands.Batch. Models.PSApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="240e5-136">Microsoft.Azure.Commands.Batch.Models.PSApplicationPackage</span></span>

## <span data-ttu-id="240e5-137">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="240e5-137">NOTES</span></span>

## <span data-ttu-id="240e5-138">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="240e5-138">RELATED LINKS</span></span>

[<span data-ttu-id="240e5-139">Get-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="240e5-139">Get-AzBatchApplication</span></span>](./Get-AzBatchApplication.md)

[<span data-ttu-id="240e5-140">Get-AzBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="240e5-140">Get-AzBatchApplicationPackage</span></span>](./Get-AzBatchApplicationPackage.md)

[<span data-ttu-id="240e5-141">New-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="240e5-141">New-AzBatchApplication</span></span>](./New-AzBatchApplication.md)

[<span data-ttu-id="240e5-142">Remove-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="240e5-142">Remove-AzBatchApplication</span></span>](./Remove-AzBatchApplication.md)

[<span data-ttu-id="240e5-143">Remove-AzBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="240e5-143">Remove-AzBatchApplicationPackage</span></span>](./Remove-AzBatchApplicationPackage.md)

[<span data-ttu-id="240e5-144">Set-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="240e5-144">Set-AzBatchApplication</span></span>](./Set-AzBatchApplication.md)


