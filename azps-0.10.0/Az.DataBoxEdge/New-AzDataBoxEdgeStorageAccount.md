---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/new-azdataboxedgestorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/DataBoxEdge/DataBoxEdge/help/New-AzDataBoxEdgeStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/DataBoxEdge/DataBoxEdge/help/New-AzDataBoxEdgeStorageAccount.md
ms.openlocfilehash: 12f77d1c2b9590ef500e1df66d36929cd359a989
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93911267"
---
# <span data-ttu-id="7b6d3-101">New-AzDataBoxEdgeStorageAccount</span><span class="sxs-lookup"><span data-stu-id="7b6d3-101">New-AzDataBoxEdgeStorageAccount</span></span>

## <span data-ttu-id="7b6d3-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="7b6d3-102">SYNOPSIS</span></span>
<span data-ttu-id="7b6d3-103">Создание новой учетной записи хранилища EDGE на устройстве.</span><span class="sxs-lookup"><span data-stu-id="7b6d3-103">Creates a new Edge Storage account in the device.</span></span>

## <span data-ttu-id="7b6d3-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="7b6d3-104">SYNTAX</span></span>

```
New-AzDataBoxEdgeStorageAccount [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 -StorageAccountCredentialName <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-Cloud] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7b6d3-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="7b6d3-105">DESCRIPTION</span></span>
<span data-ttu-id="7b6d3-106">Командлет **New-AzDataBoxEdgeStorageAccount** создает новую учетную запись хранилища EDGE на пограничном устройстве поля данных.</span><span class="sxs-lookup"><span data-stu-id="7b6d3-106">The **New-AzDataBoxEdgeStorageAccount** cmdlet creates a new Edge Storage account in a Data Box Edge device.</span></span> <span data-ttu-id="7b6d3-107">Для устройства одной учетной записью хранилища пограничного сервера можно сопоставить только с одной учетной записью облачного хранилища.</span><span class="sxs-lookup"><span data-stu-id="7b6d3-107">For a device, one Edge Storage account can be mapped at most to only one Cloud Storage account.</span></span>

## <span data-ttu-id="7b6d3-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="7b6d3-108">EXAMPLES</span></span>

### <span data-ttu-id="7b6d3-109">Пример 1</span><span class="sxs-lookup"><span data-stu-id="7b6d3-109">Example 1</span></span>
```powershell
PS C:\> New-AzDataBoxEdgeStorageAccount -ResourceGroupName resourceGroupName -DeviceName dbEdge -Name edgestoragegacount1 -StorageAccountCredentialName cloudstorageaccount1 -Cloud
Name                ContainerCount Status BlobEndpoint                                                   CloudStorageAccountName DeviceName ResourceGroupName
----                -------------- -----  ------------                                                   ----------------------- ---------- -----------------
edgestoragegacount1 0              OK     https://edgestoragegacount1.blob.dbEdge.microsoftdatabox.com/ cloudstorageaccount1     dbEdge     resourceGroupName
```

### <span data-ttu-id="7b6d3-110">Пример 2</span><span class="sxs-lookup"><span data-stu-id="7b6d3-110">Example 2</span></span>
```powershell
PS C:\> New-AzDataBoxEdgeStorageAccount -ResourceGroupName resourceGroupName -DeviceName dbEdge -Name edgestoragegacount2 -StorageAccountCredentialName cloudstorageaccount2

Name                ContainerCount Status BlobEndpoint                                                   CloudStorageAccountName DeviceName ResourceGroupName
----                -------------- -----  ------------                                                   ----------------------- ---------- -----------------
edgestoragegacount2 0              OK     https://edgestoragegacount2.blob.dbEdge.microsoftdatabox.com/ cloudstorageaccount2     dbEdge     resourceGroupName
```

<span data-ttu-id="7b6d3-111">2 EdgeStorageAccounts на устройстве не может предоставлять общий доступ к более чем одной учетной записи облачного хранилища</span><span class="sxs-lookup"><span data-stu-id="7b6d3-111">2 EdgeStorageAccounts on the device cannot share more than 1 Cloud Storage Account</span></span>

## <span data-ttu-id="7b6d3-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="7b6d3-112">PARAMETERS</span></span>

### <span data-ttu-id="7b6d3-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7b6d3-113">-AsJob</span></span>
<span data-ttu-id="7b6d3-114">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="7b6d3-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="7b6d3-115">-Cloud</span><span class="sxs-lookup"><span data-stu-id="7b6d3-115">-Cloud</span></span>
<span data-ttu-id="7b6d3-116">Будет использовать CloudStorageAccount для многоуровневых уровней</span><span class="sxs-lookup"><span data-stu-id="7b6d3-116">Will use a CloudStorageAccount for tiering</span></span>

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

### <span data-ttu-id="7b6d3-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7b6d3-117">-DefaultProfile</span></span>
<span data-ttu-id="7b6d3-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="7b6d3-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7b6d3-119">-Имя_устройства</span><span class="sxs-lookup"><span data-stu-id="7b6d3-119">-DeviceName</span></span>
<span data-ttu-id="7b6d3-120">Имя устройства</span><span class="sxs-lookup"><span data-stu-id="7b6d3-120">Device Name</span></span>

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

### <span data-ttu-id="7b6d3-121">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="7b6d3-121">-Name</span></span>
<span data-ttu-id="7b6d3-122">Название ресурса</span><span class="sxs-lookup"><span data-stu-id="7b6d3-122">Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7b6d3-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7b6d3-123">-ResourceGroupName</span></span>
<span data-ttu-id="7b6d3-124">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="7b6d3-124">Resource Group Name</span></span>

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

### <span data-ttu-id="7b6d3-125">-StorageAccountCredentialName</span><span class="sxs-lookup"><span data-stu-id="7b6d3-125">-StorageAccountCredentialName</span></span>
<span data-ttu-id="7b6d3-126">Укажите имя ресурса для существующего StorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="7b6d3-126">Provide existing StorageAccountCredential's Resource Name</span></span>

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

### <span data-ttu-id="7b6d3-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7b6d3-127">-Confirm</span></span>
<span data-ttu-id="7b6d3-128">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="7b6d3-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7b6d3-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7b6d3-129">-WhatIf</span></span>
<span data-ttu-id="7b6d3-130">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="7b6d3-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="7b6d3-131">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="7b6d3-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7b6d3-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7b6d3-132">CommonParameters</span></span>
<span data-ttu-id="7b6d3-133">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="7b6d3-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7b6d3-134">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7b6d3-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7b6d3-135">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="7b6d3-135">INPUTS</span></span>

### <span data-ttu-id="7b6d3-136">System. String</span><span class="sxs-lookup"><span data-stu-id="7b6d3-136">System.String</span></span>

### <span data-ttu-id="7b6d3-137">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="7b6d3-137">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="7b6d3-138">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="7b6d3-138">OUTPUTS</span></span>

### <span data-ttu-id="7b6d3-139">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageAccount</span><span class="sxs-lookup"><span data-stu-id="7b6d3-139">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageAccount</span></span>

## <span data-ttu-id="7b6d3-140">Пуск</span><span class="sxs-lookup"><span data-stu-id="7b6d3-140">NOTES</span></span>

## <span data-ttu-id="7b6d3-141">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="7b6d3-141">RELATED LINKS</span></span>
