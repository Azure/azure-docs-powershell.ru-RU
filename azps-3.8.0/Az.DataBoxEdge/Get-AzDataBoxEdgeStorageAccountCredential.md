---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/get-azdataboxedgestorageaccountcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Get-AzDataBoxEdgeStorageAccountCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Get-AzDataBoxEdgeStorageAccountCredential.md
ms.openlocfilehash: eca1227150741814178dbabe25caff79b3c3381e
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94073413"
---
# <span data-ttu-id="7eba0-101">Get-AzDataBoxEdgeStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="7eba0-101">Get-AzDataBoxEdgeStorageAccountCredential</span></span>

## <span data-ttu-id="7eba0-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="7eba0-102">SYNOPSIS</span></span>
<span data-ttu-id="7eba0-103">Возвращает учетные данные учетной записи хранения, соответствующие учетной записи хранения на устройстве.</span><span class="sxs-lookup"><span data-stu-id="7eba0-103">Gets the storage account credentials corresponding to the storage account on the device.</span></span>

## <span data-ttu-id="7eba0-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="7eba0-104">SYNTAX</span></span>

### <span data-ttu-id="7eba0-105">ListParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="7eba0-105">ListParameterSet (Default)</span></span>
```
Get-AzDataBoxEdgeStorageAccountCredential [-ResourceGroupName] <String> [-DeviceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7eba0-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="7eba0-106">GetByResourceIdParameterSet</span></span>
```
Get-AzDataBoxEdgeStorageAccountCredential -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="7eba0-107">GetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="7eba0-107">GetByNameParameterSet</span></span>
```
Get-AzDataBoxEdgeStorageAccountCredential [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7eba0-108">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="7eba0-108">GetByParentObjectParameterSet</span></span>
```
Get-AzDataBoxEdgeStorageAccountCredential [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>]
 -DeviceObject <PSDataBoxEdgeDevice> [<CommonParameters>]
```

## <span data-ttu-id="7eba0-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="7eba0-109">DESCRIPTION</span></span>
<span data-ttu-id="7eba0-110">Командлет **Get-AzDataBoxEdgeStorageAccountCredential** получает учетные данные учетной записи хранения для соответствующей учетной записи хранения на пограничном устройстве поля данных.</span><span class="sxs-lookup"><span data-stu-id="7eba0-110">The **Get-AzDataBoxEdgeStorageAccountCredential** cmdlet gets the storage account credentials for the corresponding storage account on the Data Box Edge device.</span></span> <span data-ttu-id="7eba0-111">Вы можете задать имя, имя группы ресурсов и параметры имени устройства, чтобы получить сведения о конкретных данных учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="7eba0-111">You can specify Name, Resource Group Name and Device Name parameters to get information about a specific storage account credential.</span></span>

## <span data-ttu-id="7eba0-112">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="7eba0-112">EXAMPLES</span></span>

### <span data-ttu-id="7eba0-113">Пример 1</span><span class="sxs-lookup"><span data-stu-id="7eba0-113">Example 1</span></span>
```powershell
PS C:\>  Get-AzDataBoxEdgeStorageAccountCredential -ResourceGroupName resourceGroupName -DeviceName deviceName
Name                          StorageAccount          SslStatus  ResourceGroupName
----------------------------- ---------------------- ---------- ---------------------
storageAccountCredentialName  StorageAccountName     Enabled    resourceGroupName
```

## <span data-ttu-id="7eba0-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="7eba0-114">PARAMETERS</span></span>

### <span data-ttu-id="7eba0-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7eba0-115">-DefaultProfile</span></span>
<span data-ttu-id="7eba0-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="7eba0-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7eba0-117">-Имя_устройства</span><span class="sxs-lookup"><span data-stu-id="7eba0-117">-DeviceName</span></span>
<span data-ttu-id="7eba0-118">Имя устройства</span><span class="sxs-lookup"><span data-stu-id="7eba0-118">Device Name</span></span>

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

### <span data-ttu-id="7eba0-119">-DeviceObject</span><span class="sxs-lookup"><span data-stu-id="7eba0-119">-DeviceObject</span></span>
<span data-ttu-id="7eba0-120">Укажите соответствующий объект устройства</span><span class="sxs-lookup"><span data-stu-id="7eba0-120">Please provide corresponding device object</span></span>

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

### <span data-ttu-id="7eba0-121">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="7eba0-121">-Name</span></span>
<span data-ttu-id="7eba0-122">Имя учетной записи хранения, которую нужно использовать</span><span class="sxs-lookup"><span data-stu-id="7eba0-122">Name of the storage account to be used</span></span>

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

### <span data-ttu-id="7eba0-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7eba0-123">-ResourceGroupName</span></span>
<span data-ttu-id="7eba0-124">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="7eba0-124">Resource Group Name</span></span>

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

### <span data-ttu-id="7eba0-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7eba0-125">-ResourceId</span></span>
<span data-ttu-id="7eba0-126">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="7eba0-126">Azure ResourceId</span></span>

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

### <span data-ttu-id="7eba0-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7eba0-127">CommonParameters</span></span>
<span data-ttu-id="7eba0-128">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="7eba0-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7eba0-129">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7eba0-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7eba0-130">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="7eba0-130">INPUTS</span></span>

### <span data-ttu-id="7eba0-131">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="7eba0-131">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice</span></span>

## <span data-ttu-id="7eba0-132">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="7eba0-132">OUTPUTS</span></span>

### <span data-ttu-id="7eba0-133">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="7eba0-133">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageAccountCredential</span></span>

## <span data-ttu-id="7eba0-134">Пуск</span><span class="sxs-lookup"><span data-stu-id="7eba0-134">NOTES</span></span>

## <span data-ttu-id="7eba0-135">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="7eba0-135">RELATED LINKS</span></span>
