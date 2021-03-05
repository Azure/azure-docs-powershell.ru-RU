---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/powershell/module/az.stackedge/get-azstackedgestorageaccountcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Get-AzStackEdgeStorageAccountCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Get-AzStackEdgeStorageAccountCredential.md
ms.openlocfilehash: efb9c7828417596afecc21fc5e5c2b2b8f7c81b8
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102007571"
---
# <span data-ttu-id="d6340-101">Get-AzStackEdgeStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="d6340-101">Get-AzStackEdgeStorageAccountCredential</span></span>

## <span data-ttu-id="d6340-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d6340-102">SYNOPSIS</span></span>
<span data-ttu-id="d6340-103">Получает учетные данные учетной записи хранения, соответствующие учетной записи хранения на устройстве.</span><span class="sxs-lookup"><span data-stu-id="d6340-103">Gets the storage account credentials corresponding to the storage account on the device.</span></span>

## <span data-ttu-id="d6340-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="d6340-104">SYNTAX</span></span>

### <span data-ttu-id="d6340-105">ListParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="d6340-105">ListParameterSet (Default)</span></span>
```
Get-AzStackEdgeStorageAccountCredential [-ResourceGroupName] <String> [-DeviceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d6340-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="d6340-106">GetByResourceIdParameterSet</span></span>
```
Get-AzStackEdgeStorageAccountCredential -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="d6340-107">GetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="d6340-107">GetByNameParameterSet</span></span>
```
Get-AzStackEdgeStorageAccountCredential [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d6340-108">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d6340-108">GetByParentObjectParameterSet</span></span>
```
Get-AzStackEdgeStorageAccountCredential [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>]
 -DeviceObject <PSStackEdgeDevice> [<CommonParameters>]
```

## <span data-ttu-id="d6340-109">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d6340-109">DESCRIPTION</span></span>
<span data-ttu-id="d6340-110">Cmdlet **Get-AzStackEdgeStorageAccountCredential** получает учетные данные учетной записи хранения для соответствующей учетной записи хранения на устройстве Stack Edge.</span><span class="sxs-lookup"><span data-stu-id="d6340-110">The **Get-AzStackEdgeStorageAccountCredential** cmdlet gets the storage account credentials for the corresponding storage account on the Stack Edge device.</span></span> <span data-ttu-id="d6340-111">Вы можете указать параметры "Имя", "Имя группы ресурсов" и "Имя устройства", чтобы получить сведения об учетных данных конкретной учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="d6340-111">You can specify Name, Resource Group Name and Device Name parameters to get information about a specific storage account credential.</span></span>

## <span data-ttu-id="d6340-112">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="d6340-112">EXAMPLES</span></span>

### <span data-ttu-id="d6340-113">Пример 1</span><span class="sxs-lookup"><span data-stu-id="d6340-113">Example 1</span></span>
```powershell
PS C:\>  Get-AzStackEdgeStorageAccountCredential -ResourceGroupName resourceGroupName -DeviceName deviceName
Name                          StorageAccount          SslStatus  ResourceGroupName
----------------------------- ---------------------- ---------- ---------------------
storageAccountCredentialName  StorageAccountName     Enabled    resourceGroupName
```

## <span data-ttu-id="d6340-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d6340-114">PARAMETERS</span></span>

### <span data-ttu-id="d6340-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d6340-115">-DefaultProfile</span></span>
<span data-ttu-id="d6340-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="d6340-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d6340-117">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="d6340-117">-DeviceName</span></span>
<span data-ttu-id="d6340-118">Имя устройства</span><span class="sxs-lookup"><span data-stu-id="d6340-118">Device Name</span></span>

```yaml
Type: System.String
Parameter Sets: ListParameterSet, GetByNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d6340-119">-DeviceObject</span><span class="sxs-lookup"><span data-stu-id="d6340-119">-DeviceObject</span></span>
<span data-ttu-id="d6340-120">Предосообщите соответствующий объект устройства</span><span class="sxs-lookup"><span data-stu-id="d6340-120">Please provide corresponding device object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeDevice
Parameter Sets: GetByParentObjectParameterSet
Aliases: Device

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d6340-121">-Name</span><span class="sxs-lookup"><span data-stu-id="d6340-121">-Name</span></span>
<span data-ttu-id="d6340-122">Имя используемой учетной записи хранения</span><span class="sxs-lookup"><span data-stu-id="d6340-122">Name of the storage account to be used</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases: StorageAccountCredentialName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: GetByParentObjectParameterSet
Aliases: StorageAccountCredentialName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d6340-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d6340-123">-ResourceGroupName</span></span>
<span data-ttu-id="d6340-124">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="d6340-124">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: ListParameterSet, GetByNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d6340-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d6340-125">-ResourceId</span></span>
<span data-ttu-id="d6340-126">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="d6340-126">Azure ResourceId</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d6340-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d6340-127">CommonParameters</span></span>
<span data-ttu-id="d6340-128">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d6340-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d6340-129">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d6340-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d6340-130">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d6340-130">INPUTS</span></span>

### <span data-ttu-id="d6340-131">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="d6340-131">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeDevice</span></span>

## <span data-ttu-id="d6340-132">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="d6340-132">OUTPUTS</span></span>

### <span data-ttu-id="d6340-133">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="d6340-133">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeStorageAccountCredential</span></span>

## <span data-ttu-id="d6340-134">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="d6340-134">NOTES</span></span>

## <span data-ttu-id="d6340-135">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d6340-135">RELATED LINKS</span></span>
