---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: FD2E3442-9CEA-4390-BE9C-772C7D6FD1E2
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/remove-azbatchapplicationpackage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Remove-AzBatchApplicationPackage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Remove-AzBatchApplicationPackage.md
ms.openlocfilehash: f88994649281d442f37a2bafa2cf2b4f74e6b86e
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98411495"
---
# <span data-ttu-id="63df0-101">Remove-AzBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="63df0-101">Remove-AzBatchApplicationPackage</span></span>

## <span data-ttu-id="63df0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="63df0-102">SYNOPSIS</span></span>
<span data-ttu-id="63df0-103">Удаляет запись пакета приложения и двоичный файл.</span><span class="sxs-lookup"><span data-stu-id="63df0-103">Deletes an application package record and the binary file.</span></span>

## <span data-ttu-id="63df0-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="63df0-104">SYNTAX</span></span>

```
Remove-AzBatchApplicationPackage [-AccountName] <String> [-ResourceGroupName] <String>
 [-ApplicationName] <String> [-ApplicationVersion] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="63df0-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="63df0-105">DESCRIPTION</span></span>
<span data-ttu-id="63df0-106">При **этом из учетной** записи Azure Batch удаляются запись пакета приложения и двоичный файл.</span><span class="sxs-lookup"><span data-stu-id="63df0-106">The **Remove-AzBatchApplicationPackage** cmdlet deletes an application package record and the binary file from an Azure Batch account.</span></span>

## <span data-ttu-id="63df0-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="63df0-107">EXAMPLES</span></span>

### <span data-ttu-id="63df0-108">Пример 1. Удаление пакета приложения из учетной записи пакета</span><span class="sxs-lookup"><span data-stu-id="63df0-108">Example 1: Delete an application package from a Batch account</span></span>
```
PS C:\>Remove-AzBatchApplicationPackage -AccountName "ContosoBatch" -ResourceGroupName "ContosoBatchGroup" -ApplicationName "litware" -ApplicationVersion "1.0"
```

<span data-ttu-id="63df0-109">Эта команда удаляет приложение Litware версии 1.0 из учетной записи ContosoBatchGroup.</span><span class="sxs-lookup"><span data-stu-id="63df0-109">This command deletes version 1.0 of the Litware application from the ContosoBatchGroup account.</span></span>
<span data-ttu-id="63df0-110">Эта команда удаляет как запись пакета, так и двоичный файл пакета.</span><span class="sxs-lookup"><span data-stu-id="63df0-110">The command deletes both the package record and the blob that contain the package binary file.</span></span>

## <span data-ttu-id="63df0-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="63df0-111">PARAMETERS</span></span>

### <span data-ttu-id="63df0-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="63df0-112">-AccountName</span></span>
<span data-ttu-id="63df0-113">Имя учетной записи пакета, из которой этот cmdlet удаляет пакет приложения.</span><span class="sxs-lookup"><span data-stu-id="63df0-113">Specifies the name of the Batch account from which this cmdlet deletes an application package.</span></span>

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

### <span data-ttu-id="63df0-114">-ApplicationName</span><span class="sxs-lookup"><span data-stu-id="63df0-114">-ApplicationName</span></span>
<span data-ttu-id="63df0-115">Указывает имя приложения.</span><span class="sxs-lookup"><span data-stu-id="63df0-115">Specifies the name of the application.</span></span>

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

### <span data-ttu-id="63df0-116">-ApplicationVersion</span><span class="sxs-lookup"><span data-stu-id="63df0-116">-ApplicationVersion</span></span>
<span data-ttu-id="63df0-117">Определяет версию приложения.</span><span class="sxs-lookup"><span data-stu-id="63df0-117">Specifies the version of the application.</span></span>

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

### <span data-ttu-id="63df0-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="63df0-118">-DefaultProfile</span></span>
<span data-ttu-id="63df0-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="63df0-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="63df0-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="63df0-120">-ResourceGroupName</span></span>
<span data-ttu-id="63df0-121">Имя группы ресурсов, которая содержит учетную запись пакета.</span><span class="sxs-lookup"><span data-stu-id="63df0-121">Specifies the name of the resource group that contains the Batch account.</span></span>

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

### <span data-ttu-id="63df0-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="63df0-122">CommonParameters</span></span>
<span data-ttu-id="63df0-123">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="63df0-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="63df0-124">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="63df0-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="63df0-125">INPUTS</span><span class="sxs-lookup"><span data-stu-id="63df0-125">INPUTS</span></span>

### <span data-ttu-id="63df0-126">System.String</span><span class="sxs-lookup"><span data-stu-id="63df0-126">System.String</span></span>

## <span data-ttu-id="63df0-127">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="63df0-127">OUTPUTS</span></span>

### <span data-ttu-id="63df0-128">System.Void</span><span class="sxs-lookup"><span data-stu-id="63df0-128">System.Void</span></span>

## <span data-ttu-id="63df0-129">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="63df0-129">NOTES</span></span>

## <span data-ttu-id="63df0-130">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="63df0-130">RELATED LINKS</span></span>

[<span data-ttu-id="63df0-131">Get-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="63df0-131">Get-AzBatchApplication</span></span>](./Get-AzBatchApplication.md)

[<span data-ttu-id="63df0-132">Get-AzBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="63df0-132">Get-AzBatchApplicationPackage</span></span>](./Get-AzBatchApplicationPackage.md)

[<span data-ttu-id="63df0-133">New-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="63df0-133">New-AzBatchApplication</span></span>](./New-AzBatchApplication.md)

[<span data-ttu-id="63df0-134">New-AzBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="63df0-134">New-AzBatchApplicationPackage</span></span>](./New-AzBatchApplicationPackage.md)

[<span data-ttu-id="63df0-135">Remove-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="63df0-135">Remove-AzBatchApplication</span></span>](./Remove-AzBatchApplication.md)

[<span data-ttu-id="63df0-136">Set-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="63df0-136">Set-AzBatchApplication</span></span>](./Set-AzBatchApplication.md)


