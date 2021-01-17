---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/new-azstackedgestorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/New-AzStackEdgeStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/New-AzStackEdgeStorageAccount.md
ms.openlocfilehash: 815b8a7feb22e754302c455c7666f8408c348c92
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98395911"
---
# <span data-ttu-id="e0891-101">New-AzStackEdgeStorageAccount</span><span class="sxs-lookup"><span data-stu-id="e0891-101">New-AzStackEdgeStorageAccount</span></span>

## <span data-ttu-id="e0891-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e0891-102">SYNOPSIS</span></span>
<span data-ttu-id="e0891-103">Создает новую учетную запись edge Storage на устройстве.</span><span class="sxs-lookup"><span data-stu-id="e0891-103">Creates a new Edge Storage account in the device.</span></span>

## <span data-ttu-id="e0891-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="e0891-104">SYNTAX</span></span>

```
New-AzStackEdgeStorageAccount [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 -StorageAccountCredentialName <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-Cloud] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e0891-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e0891-105">DESCRIPTION</span></span>
<span data-ttu-id="e0891-106">С его учетной записью в устройстве Stack Edge создается учетная запись хранилища **New-AzStackEdgeStorageAccount.**</span><span class="sxs-lookup"><span data-stu-id="e0891-106">The **New-AzStackEdgeStorageAccount** cmdlet creates a new Edge Storage account in a Stack Edge device.</span></span> <span data-ttu-id="e0891-107">На устройстве одну учетную запись edge Storage можно как можно соотнося только с одной учетной записью облачного хранилища.</span><span class="sxs-lookup"><span data-stu-id="e0891-107">For a device, one Edge Storage account can be mapped at most to only one Cloud Storage account.</span></span>

## <span data-ttu-id="e0891-108">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="e0891-108">EXAMPLES</span></span>

### <span data-ttu-id="e0891-109">Пример 1</span><span class="sxs-lookup"><span data-stu-id="e0891-109">Example 1</span></span>
```powershell
PS C:\> New-AzStackEdgeStorageAccount -ResourceGroupName resourceGroupName -DeviceName dbEdge -Name edgestoragegacount1 -StorageAccountCredentialName cloudstorageaccount1 -Cloud
Name                ContainerCount Status BlobEndpoint                                                   CloudStorageAccountName DeviceName ResourceGroupName
----                -------------- -----  ------------                                                   ----------------------- ---------- -----------------
edgestoragegacount1 0              OK     https://edgestoragegacount1.blob.dbEdge.microsoftdatabox.com/ cloudstorageaccount1     dbEdge     resourceGroupName
```

### <span data-ttu-id="e0891-110">Пример 2</span><span class="sxs-lookup"><span data-stu-id="e0891-110">Example 2</span></span>
```powershell
PS C:\> New-AzStackEdgeStorageAccount -ResourceGroupName resourceGroupName -DeviceName dbEdge -Name edgestoragegacount2 -StorageAccountCredentialName cloudstorageaccount2

Name                ContainerCount Status BlobEndpoint                                                   CloudStorageAccountName DeviceName ResourceGroupName
----                -------------- -----  ------------                                                   ----------------------- ---------- -----------------
edgestoragegacount2 0              OK     https://edgestoragegacount2.blob.dbEdge.microsoftdatabox.com/ cloudstorageaccount2     dbEdge     resourceGroupName
```

<span data-ttu-id="e0891-111">2 EdgeStorageAccounts на устройстве не могут делиться более чем 1 учетной записью облачного хранилища</span><span class="sxs-lookup"><span data-stu-id="e0891-111">2 EdgeStorageAccounts on the device cannot share more than 1 Cloud Storage Account</span></span>

## <span data-ttu-id="e0891-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e0891-112">PARAMETERS</span></span>

### <span data-ttu-id="e0891-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e0891-113">-AsJob</span></span>
<span data-ttu-id="e0891-114">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="e0891-114">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e0891-115">-Облако</span><span class="sxs-lookup"><span data-stu-id="e0891-115">-Cloud</span></span>
<span data-ttu-id="e0891-116">Будет использовать CloudStorageAccount для многоуровневого</span><span class="sxs-lookup"><span data-stu-id="e0891-116">Will use a CloudStorageAccount for tiering</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e0891-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e0891-117">-DefaultProfile</span></span>
<span data-ttu-id="e0891-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="e0891-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e0891-119">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="e0891-119">-DeviceName</span></span>
<span data-ttu-id="e0891-120">Имя устройства</span><span class="sxs-lookup"><span data-stu-id="e0891-120">Device Name</span></span>

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

### <span data-ttu-id="e0891-121">-Name</span><span class="sxs-lookup"><span data-stu-id="e0891-121">-Name</span></span>
<span data-ttu-id="e0891-122">Название ресурса</span><span class="sxs-lookup"><span data-stu-id="e0891-122">Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: EdgeStorageAccount

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e0891-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e0891-123">-ResourceGroupName</span></span>
<span data-ttu-id="e0891-124">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="e0891-124">Resource Group Name</span></span>

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

### <span data-ttu-id="e0891-125">-StorageAccountCredentialName</span><span class="sxs-lookup"><span data-stu-id="e0891-125">-StorageAccountCredentialName</span></span>
<span data-ttu-id="e0891-126">Предоставление имени ресурса существующего хранилищаAccountCredential</span><span class="sxs-lookup"><span data-stu-id="e0891-126">Provide existing StorageAccountCredential's Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e0891-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e0891-127">-Confirm</span></span>
<span data-ttu-id="e0891-128">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e0891-128">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e0891-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e0891-129">-WhatIf</span></span>
<span data-ttu-id="e0891-130">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e0891-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e0891-131">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="e0891-131">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e0891-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e0891-132">CommonParameters</span></span>
<span data-ttu-id="e0891-133">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e0891-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e0891-134">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e0891-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e0891-135">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e0891-135">INPUTS</span></span>

### <span data-ttu-id="e0891-136">System.String</span><span class="sxs-lookup"><span data-stu-id="e0891-136">System.String</span></span>

### <span data-ttu-id="e0891-137">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="e0891-137">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="e0891-138">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="e0891-138">OUTPUTS</span></span>

### <span data-ttu-id="e0891-139">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeStorageAccount</span><span class="sxs-lookup"><span data-stu-id="e0891-139">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeStorageAccount</span></span>

## <span data-ttu-id="e0891-140">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="e0891-140">NOTES</span></span>

## <span data-ttu-id="e0891-141">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e0891-141">RELATED LINKS</span></span>
