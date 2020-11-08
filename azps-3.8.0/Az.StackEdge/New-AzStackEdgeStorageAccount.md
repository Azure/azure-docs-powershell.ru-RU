---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/new-azstackedgestorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/New-AzStackEdgeStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/New-AzStackEdgeStorageAccount.md
ms.openlocfilehash: 815b8a7feb22e754302c455c7666f8408c348c92
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94073067"
---
# <span data-ttu-id="8a992-101">New-AzStackEdgeStorageAccount</span><span class="sxs-lookup"><span data-stu-id="8a992-101">New-AzStackEdgeStorageAccount</span></span>

## <span data-ttu-id="8a992-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="8a992-102">SYNOPSIS</span></span>
<span data-ttu-id="8a992-103">Создание новой учетной записи хранилища EDGE на устройстве.</span><span class="sxs-lookup"><span data-stu-id="8a992-103">Creates a new Edge Storage account in the device.</span></span>

## <span data-ttu-id="8a992-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="8a992-104">SYNTAX</span></span>

```
New-AzStackEdgeStorageAccount [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 -StorageAccountCredentialName <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-Cloud] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8a992-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="8a992-105">DESCRIPTION</span></span>
<span data-ttu-id="8a992-106">Командлет **New-AzStackEdgeStorageAccount** создает новую учетную запись хранилища EDGE на пограничном устройстве стопки.</span><span class="sxs-lookup"><span data-stu-id="8a992-106">The **New-AzStackEdgeStorageAccount** cmdlet creates a new Edge Storage account in a Stack Edge device.</span></span> <span data-ttu-id="8a992-107">Для устройства одной учетной записью хранилища пограничного сервера можно сопоставить только с одной учетной записью облачного хранилища.</span><span class="sxs-lookup"><span data-stu-id="8a992-107">For a device, one Edge Storage account can be mapped at most to only one Cloud Storage account.</span></span>

## <span data-ttu-id="8a992-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="8a992-108">EXAMPLES</span></span>

### <span data-ttu-id="8a992-109">Пример 1</span><span class="sxs-lookup"><span data-stu-id="8a992-109">Example 1</span></span>
```powershell
PS C:\> New-AzStackEdgeStorageAccount -ResourceGroupName resourceGroupName -DeviceName dbEdge -Name edgestoragegacount1 -StorageAccountCredentialName cloudstorageaccount1 -Cloud
Name                ContainerCount Status BlobEndpoint                                                   CloudStorageAccountName DeviceName ResourceGroupName
----                -------------- -----  ------------                                                   ----------------------- ---------- -----------------
edgestoragegacount1 0              OK     https://edgestoragegacount1.blob.dbEdge.microsoftdatabox.com/ cloudstorageaccount1     dbEdge     resourceGroupName
```

### <span data-ttu-id="8a992-110">Пример 2</span><span class="sxs-lookup"><span data-stu-id="8a992-110">Example 2</span></span>
```powershell
PS C:\> New-AzStackEdgeStorageAccount -ResourceGroupName resourceGroupName -DeviceName dbEdge -Name edgestoragegacount2 -StorageAccountCredentialName cloudstorageaccount2

Name                ContainerCount Status BlobEndpoint                                                   CloudStorageAccountName DeviceName ResourceGroupName
----                -------------- -----  ------------                                                   ----------------------- ---------- -----------------
edgestoragegacount2 0              OK     https://edgestoragegacount2.blob.dbEdge.microsoftdatabox.com/ cloudstorageaccount2     dbEdge     resourceGroupName
```

<span data-ttu-id="8a992-111">2 EdgeStorageAccounts на устройстве не может предоставлять общий доступ к более чем одной учетной записи облачного хранилища</span><span class="sxs-lookup"><span data-stu-id="8a992-111">2 EdgeStorageAccounts on the device cannot share more than 1 Cloud Storage Account</span></span>

## <span data-ttu-id="8a992-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="8a992-112">PARAMETERS</span></span>

### <span data-ttu-id="8a992-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8a992-113">-AsJob</span></span>
<span data-ttu-id="8a992-114">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="8a992-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="8a992-115">-Cloud</span><span class="sxs-lookup"><span data-stu-id="8a992-115">-Cloud</span></span>
<span data-ttu-id="8a992-116">Будет использовать CloudStorageAccount для многоуровневых уровней</span><span class="sxs-lookup"><span data-stu-id="8a992-116">Will use a CloudStorageAccount for tiering</span></span>

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

### <span data-ttu-id="8a992-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8a992-117">-DefaultProfile</span></span>
<span data-ttu-id="8a992-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="8a992-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8a992-119">-Имя_устройства</span><span class="sxs-lookup"><span data-stu-id="8a992-119">-DeviceName</span></span>
<span data-ttu-id="8a992-120">Имя устройства</span><span class="sxs-lookup"><span data-stu-id="8a992-120">Device Name</span></span>

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

### <span data-ttu-id="8a992-121">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="8a992-121">-Name</span></span>
<span data-ttu-id="8a992-122">Название ресурса</span><span class="sxs-lookup"><span data-stu-id="8a992-122">Resource Name</span></span>

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

### <span data-ttu-id="8a992-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8a992-123">-ResourceGroupName</span></span>
<span data-ttu-id="8a992-124">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="8a992-124">Resource Group Name</span></span>

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

### <span data-ttu-id="8a992-125">-StorageAccountCredentialName</span><span class="sxs-lookup"><span data-stu-id="8a992-125">-StorageAccountCredentialName</span></span>
<span data-ttu-id="8a992-126">Укажите имя ресурса для существующего StorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="8a992-126">Provide existing StorageAccountCredential's Resource Name</span></span>

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

### <span data-ttu-id="8a992-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8a992-127">-Confirm</span></span>
<span data-ttu-id="8a992-128">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="8a992-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8a992-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8a992-129">-WhatIf</span></span>
<span data-ttu-id="8a992-130">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="8a992-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="8a992-131">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="8a992-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8a992-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8a992-132">CommonParameters</span></span>
<span data-ttu-id="8a992-133">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="8a992-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8a992-134">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8a992-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8a992-135">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="8a992-135">INPUTS</span></span>

### <span data-ttu-id="8a992-136">System. String</span><span class="sxs-lookup"><span data-stu-id="8a992-136">System.String</span></span>

### <span data-ttu-id="8a992-137">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="8a992-137">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="8a992-138">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="8a992-138">OUTPUTS</span></span>

### <span data-ttu-id="8a992-139">Microsoft. Azure. PowerShell. командлеты. StackEdge. Models. PSStackEdgeStorageAccount</span><span class="sxs-lookup"><span data-stu-id="8a992-139">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeStorageAccount</span></span>

## <span data-ttu-id="8a992-140">Пуск</span><span class="sxs-lookup"><span data-stu-id="8a992-140">NOTES</span></span>

## <span data-ttu-id="8a992-141">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="8a992-141">RELATED LINKS</span></span>
