---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/new-azstackedgestorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/New-AzStackEdgeStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/New-AzStackEdgeStorageAccount.md
ms.openlocfilehash: 815b8a7feb22e754302c455c7666f8408c348c92
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100221932"
---
# <span data-ttu-id="1784f-101">New-AzStackEdgeStorageAccount</span><span class="sxs-lookup"><span data-stu-id="1784f-101">New-AzStackEdgeStorageAccount</span></span>

## <span data-ttu-id="1784f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1784f-102">SYNOPSIS</span></span>
<span data-ttu-id="1784f-103">Создает на устройстве новую учетную запись edge Storage.</span><span class="sxs-lookup"><span data-stu-id="1784f-103">Creates a new Edge Storage account in the device.</span></span>

## <span data-ttu-id="1784f-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="1784f-104">SYNTAX</span></span>

```
New-AzStackEdgeStorageAccount [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 -StorageAccountCredentialName <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-Cloud] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1784f-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="1784f-105">DESCRIPTION</span></span>
<span data-ttu-id="1784f-106">С его учетной записью в устройстве Stack Edge создается учетная запись хранилища **New-AzStackEdgeStorageAccount.**</span><span class="sxs-lookup"><span data-stu-id="1784f-106">The **New-AzStackEdgeStorageAccount** cmdlet creates a new Edge Storage account in a Stack Edge device.</span></span> <span data-ttu-id="1784f-107">На устройстве одну учетную запись edge Storage можно как можно соотнося только с одной учетной записью облачного хранилища.</span><span class="sxs-lookup"><span data-stu-id="1784f-107">For a device, one Edge Storage account can be mapped at most to only one Cloud Storage account.</span></span>

## <span data-ttu-id="1784f-108">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="1784f-108">EXAMPLES</span></span>

### <span data-ttu-id="1784f-109">Пример 1</span><span class="sxs-lookup"><span data-stu-id="1784f-109">Example 1</span></span>
```powershell
PS C:\> New-AzStackEdgeStorageAccount -ResourceGroupName resourceGroupName -DeviceName dbEdge -Name edgestoragegacount1 -StorageAccountCredentialName cloudstorageaccount1 -Cloud
Name                ContainerCount Status BlobEndpoint                                                   CloudStorageAccountName DeviceName ResourceGroupName
----                -------------- -----  ------------                                                   ----------------------- ---------- -----------------
edgestoragegacount1 0              OK     https://edgestoragegacount1.blob.dbEdge.microsoftdatabox.com/ cloudstorageaccount1     dbEdge     resourceGroupName
```

### <span data-ttu-id="1784f-110">Пример 2</span><span class="sxs-lookup"><span data-stu-id="1784f-110">Example 2</span></span>
```powershell
PS C:\> New-AzStackEdgeStorageAccount -ResourceGroupName resourceGroupName -DeviceName dbEdge -Name edgestoragegacount2 -StorageAccountCredentialName cloudstorageaccount2

Name                ContainerCount Status BlobEndpoint                                                   CloudStorageAccountName DeviceName ResourceGroupName
----                -------------- -----  ------------                                                   ----------------------- ---------- -----------------
edgestoragegacount2 0              OK     https://edgestoragegacount2.blob.dbEdge.microsoftdatabox.com/ cloudstorageaccount2     dbEdge     resourceGroupName
```

<span data-ttu-id="1784f-111">2 EdgeStorageAccounts на устройстве не могут делиться более чем 1 учетной записью облачного хранилища</span><span class="sxs-lookup"><span data-stu-id="1784f-111">2 EdgeStorageAccounts on the device cannot share more than 1 Cloud Storage Account</span></span>

## <span data-ttu-id="1784f-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1784f-112">PARAMETERS</span></span>

### <span data-ttu-id="1784f-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1784f-113">-AsJob</span></span>
<span data-ttu-id="1784f-114">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="1784f-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="1784f-115">-Cloud</span><span class="sxs-lookup"><span data-stu-id="1784f-115">-Cloud</span></span>
<span data-ttu-id="1784f-116">Будет использовать CloudStorageAccount для многоуровневого</span><span class="sxs-lookup"><span data-stu-id="1784f-116">Will use a CloudStorageAccount for tiering</span></span>

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

### <span data-ttu-id="1784f-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1784f-117">-DefaultProfile</span></span>
<span data-ttu-id="1784f-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="1784f-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1784f-119">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="1784f-119">-DeviceName</span></span>
<span data-ttu-id="1784f-120">Имя устройства</span><span class="sxs-lookup"><span data-stu-id="1784f-120">Device Name</span></span>

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

### <span data-ttu-id="1784f-121">-Name</span><span class="sxs-lookup"><span data-stu-id="1784f-121">-Name</span></span>
<span data-ttu-id="1784f-122">Название ресурса</span><span class="sxs-lookup"><span data-stu-id="1784f-122">Resource Name</span></span>

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

### <span data-ttu-id="1784f-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1784f-123">-ResourceGroupName</span></span>
<span data-ttu-id="1784f-124">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="1784f-124">Resource Group Name</span></span>

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

### <span data-ttu-id="1784f-125">-StorageAccountCredentialName</span><span class="sxs-lookup"><span data-stu-id="1784f-125">-StorageAccountCredentialName</span></span>
<span data-ttu-id="1784f-126">Предоставление имени ресурса существующего хранилищаAccountCredential</span><span class="sxs-lookup"><span data-stu-id="1784f-126">Provide existing StorageAccountCredential's Resource Name</span></span>

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

### <span data-ttu-id="1784f-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1784f-127">-Confirm</span></span>
<span data-ttu-id="1784f-128">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="1784f-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1784f-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1784f-129">-WhatIf</span></span>
<span data-ttu-id="1784f-130">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1784f-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="1784f-131">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="1784f-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1784f-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1784f-132">CommonParameters</span></span>
<span data-ttu-id="1784f-133">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1784f-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1784f-134">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1784f-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1784f-135">INPUTS</span><span class="sxs-lookup"><span data-stu-id="1784f-135">INPUTS</span></span>

### <span data-ttu-id="1784f-136">System.String</span><span class="sxs-lookup"><span data-stu-id="1784f-136">System.String</span></span>

### <span data-ttu-id="1784f-137">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="1784f-137">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="1784f-138">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="1784f-138">OUTPUTS</span></span>

### <span data-ttu-id="1784f-139">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeStorageAccount</span><span class="sxs-lookup"><span data-stu-id="1784f-139">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeStorageAccount</span></span>

## <span data-ttu-id="1784f-140">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="1784f-140">NOTES</span></span>

## <span data-ttu-id="1784f-141">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="1784f-141">RELATED LINKS</span></span>
