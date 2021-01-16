---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/get-azdataboxedgestorageaccountcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Get-AzDataBoxEdgeStorageAccountCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Get-AzDataBoxEdgeStorageAccountCredential.md
ms.openlocfilehash: eca1227150741814178dbabe25caff79b3c3381e
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98508633"
---
# <span data-ttu-id="23934-101">Get-AzDataBoxEdgeStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="23934-101">Get-AzDataBoxEdgeStorageAccountCredential</span></span>

## <span data-ttu-id="23934-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="23934-102">SYNOPSIS</span></span>
<span data-ttu-id="23934-103">Получает учетные данные учетной записи хранения, соответствующие учетной записи хранения на устройстве.</span><span class="sxs-lookup"><span data-stu-id="23934-103">Gets the storage account credentials corresponding to the storage account on the device.</span></span>

## <span data-ttu-id="23934-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="23934-104">SYNTAX</span></span>

### <span data-ttu-id="23934-105">ListParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="23934-105">ListParameterSet (Default)</span></span>
```
Get-AzDataBoxEdgeStorageAccountCredential [-ResourceGroupName] <String> [-DeviceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="23934-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="23934-106">GetByResourceIdParameterSet</span></span>
```
Get-AzDataBoxEdgeStorageAccountCredential -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="23934-107">GetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="23934-107">GetByNameParameterSet</span></span>
```
Get-AzDataBoxEdgeStorageAccountCredential [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="23934-108">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="23934-108">GetByParentObjectParameterSet</span></span>
```
Get-AzDataBoxEdgeStorageAccountCredential [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>]
 -DeviceObject <PSDataBoxEdgeDevice> [<CommonParameters>]
```

## <span data-ttu-id="23934-109">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="23934-109">DESCRIPTION</span></span>
<span data-ttu-id="23934-110">**Cmdlet Get-AzDataBoxEdgeStorageAccountCredential** получает учетные данные учетной записи хранения для соответствующей учетной записи хранения на устройстве Edge Box Data Box.</span><span class="sxs-lookup"><span data-stu-id="23934-110">The **Get-AzDataBoxEdgeStorageAccountCredential** cmdlet gets the storage account credentials for the corresponding storage account on the Data Box Edge device.</span></span> <span data-ttu-id="23934-111">Вы можете указать параметры "Имя", "Имя группы ресурсов" и "Имя устройства", чтобы получить сведения об учетных данных конкретной учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="23934-111">You can specify Name, Resource Group Name and Device Name parameters to get information about a specific storage account credential.</span></span>

## <span data-ttu-id="23934-112">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="23934-112">EXAMPLES</span></span>

### <span data-ttu-id="23934-113">Пример 1</span><span class="sxs-lookup"><span data-stu-id="23934-113">Example 1</span></span>
```powershell
PS C:\>  Get-AzDataBoxEdgeStorageAccountCredential -ResourceGroupName resourceGroupName -DeviceName deviceName
Name                          StorageAccount          SslStatus  ResourceGroupName
----------------------------- ---------------------- ---------- ---------------------
storageAccountCredentialName  StorageAccountName     Enabled    resourceGroupName
```

## <span data-ttu-id="23934-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="23934-114">PARAMETERS</span></span>

### <span data-ttu-id="23934-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="23934-115">-DefaultProfile</span></span>
<span data-ttu-id="23934-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="23934-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="23934-117">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="23934-117">-DeviceName</span></span>
<span data-ttu-id="23934-118">Имя устройства</span><span class="sxs-lookup"><span data-stu-id="23934-118">Device Name</span></span>

```yaml
Type: System.String
Parameter Sets: ListParameterSet, GetByNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="23934-119">-DeviceObject</span><span class="sxs-lookup"><span data-stu-id="23934-119">-DeviceObject</span></span>
<span data-ttu-id="23934-120">Предосообщите соответствующий объект устройства</span><span class="sxs-lookup"><span data-stu-id="23934-120">Please provide corresponding device object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice
Parameter Sets: GetByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="23934-121">-Name</span><span class="sxs-lookup"><span data-stu-id="23934-121">-Name</span></span>
<span data-ttu-id="23934-122">Имя используемой учетной записи хранения</span><span class="sxs-lookup"><span data-stu-id="23934-122">Name of the storage account to be used</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: GetByParentObjectParameterSet
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="23934-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="23934-123">-ResourceGroupName</span></span>
<span data-ttu-id="23934-124">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="23934-124">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: ListParameterSet, GetByNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="23934-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="23934-125">-ResourceId</span></span>
<span data-ttu-id="23934-126">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="23934-126">Azure ResourceId</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="23934-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="23934-127">CommonParameters</span></span>
<span data-ttu-id="23934-128">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="23934-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="23934-129">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="23934-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="23934-130">INPUTS</span><span class="sxs-lookup"><span data-stu-id="23934-130">INPUTS</span></span>

### <span data-ttu-id="23934-131">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDAtaBoxEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="23934-131">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice</span></span>

## <span data-ttu-id="23934-132">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="23934-132">OUTPUTS</span></span>

### <span data-ttu-id="23934-133">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="23934-133">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageAccountCredential</span></span>

## <span data-ttu-id="23934-134">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="23934-134">NOTES</span></span>

## <span data-ttu-id="23934-135">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="23934-135">RELATED LINKS</span></span>