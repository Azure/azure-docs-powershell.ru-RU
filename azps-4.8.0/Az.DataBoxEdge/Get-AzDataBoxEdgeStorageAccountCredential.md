---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/get-azdataboxedgestorageaccountcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Get-AzDataBoxEdgeStorageAccountCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Get-AzDataBoxEdgeStorageAccountCredential.md
ms.openlocfilehash: eca1227150741814178dbabe25caff79b3c3381e
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94236822"
---
# <span data-ttu-id="a0c49-101">Get-AzDataBoxEdgeStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="a0c49-101">Get-AzDataBoxEdgeStorageAccountCredential</span></span>

## <span data-ttu-id="a0c49-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="a0c49-102">SYNOPSIS</span></span>
<span data-ttu-id="a0c49-103">Возвращает учетные данные учетной записи хранения, соответствующие учетной записи хранения на устройстве.</span><span class="sxs-lookup"><span data-stu-id="a0c49-103">Gets the storage account credentials corresponding to the storage account on the device.</span></span>

## <span data-ttu-id="a0c49-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="a0c49-104">SYNTAX</span></span>

### <span data-ttu-id="a0c49-105">ListParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="a0c49-105">ListParameterSet (Default)</span></span>
```
Get-AzDataBoxEdgeStorageAccountCredential [-ResourceGroupName] <String> [-DeviceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a0c49-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a0c49-106">GetByResourceIdParameterSet</span></span>
```
Get-AzDataBoxEdgeStorageAccountCredential -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="a0c49-107">GetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="a0c49-107">GetByNameParameterSet</span></span>
```
Get-AzDataBoxEdgeStorageAccountCredential [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a0c49-108">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a0c49-108">GetByParentObjectParameterSet</span></span>
```
Get-AzDataBoxEdgeStorageAccountCredential [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>]
 -DeviceObject <PSDataBoxEdgeDevice> [<CommonParameters>]
```

## <span data-ttu-id="a0c49-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a0c49-109">DESCRIPTION</span></span>
<span data-ttu-id="a0c49-110">Командлет **Get-AzDataBoxEdgeStorageAccountCredential** получает учетные данные учетной записи хранения для соответствующей учетной записи хранения на пограничном устройстве поля данных.</span><span class="sxs-lookup"><span data-stu-id="a0c49-110">The **Get-AzDataBoxEdgeStorageAccountCredential** cmdlet gets the storage account credentials for the corresponding storage account on the Data Box Edge device.</span></span> <span data-ttu-id="a0c49-111">Вы можете задать имя, имя группы ресурсов и параметры имени устройства, чтобы получить сведения о конкретных данных учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="a0c49-111">You can specify Name, Resource Group Name and Device Name parameters to get information about a specific storage account credential.</span></span>

## <span data-ttu-id="a0c49-112">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="a0c49-112">EXAMPLES</span></span>

### <span data-ttu-id="a0c49-113">Пример 1</span><span class="sxs-lookup"><span data-stu-id="a0c49-113">Example 1</span></span>
```powershell
PS C:\>  Get-AzDataBoxEdgeStorageAccountCredential -ResourceGroupName resourceGroupName -DeviceName deviceName
Name                          StorageAccount          SslStatus  ResourceGroupName
----------------------------- ---------------------- ---------- ---------------------
storageAccountCredentialName  StorageAccountName     Enabled    resourceGroupName
```

## <span data-ttu-id="a0c49-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="a0c49-114">PARAMETERS</span></span>

### <span data-ttu-id="a0c49-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a0c49-115">-DefaultProfile</span></span>
<span data-ttu-id="a0c49-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="a0c49-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a0c49-117">-Имя_устройства</span><span class="sxs-lookup"><span data-stu-id="a0c49-117">-DeviceName</span></span>
<span data-ttu-id="a0c49-118">Имя устройства</span><span class="sxs-lookup"><span data-stu-id="a0c49-118">Device Name</span></span>

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

### <span data-ttu-id="a0c49-119">-DeviceObject</span><span class="sxs-lookup"><span data-stu-id="a0c49-119">-DeviceObject</span></span>
<span data-ttu-id="a0c49-120">Укажите соответствующий объект устройства</span><span class="sxs-lookup"><span data-stu-id="a0c49-120">Please provide corresponding device object</span></span>

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

### <span data-ttu-id="a0c49-121">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="a0c49-121">-Name</span></span>
<span data-ttu-id="a0c49-122">Имя учетной записи хранения, которую нужно использовать</span><span class="sxs-lookup"><span data-stu-id="a0c49-122">Name of the storage account to be used</span></span>

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

### <span data-ttu-id="a0c49-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a0c49-123">-ResourceGroupName</span></span>
<span data-ttu-id="a0c49-124">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="a0c49-124">Resource Group Name</span></span>

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

### <span data-ttu-id="a0c49-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a0c49-125">-ResourceId</span></span>
<span data-ttu-id="a0c49-126">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="a0c49-126">Azure ResourceId</span></span>

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

### <span data-ttu-id="a0c49-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a0c49-127">CommonParameters</span></span>
<span data-ttu-id="a0c49-128">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="a0c49-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a0c49-129">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a0c49-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a0c49-130">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="a0c49-130">INPUTS</span></span>

### <span data-ttu-id="a0c49-131">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="a0c49-131">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice</span></span>

## <span data-ttu-id="a0c49-132">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="a0c49-132">OUTPUTS</span></span>

### <span data-ttu-id="a0c49-133">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="a0c49-133">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageAccountCredential</span></span>

## <span data-ttu-id="a0c49-134">Пуск</span><span class="sxs-lookup"><span data-stu-id="a0c49-134">NOTES</span></span>

## <span data-ttu-id="a0c49-135">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a0c49-135">RELATED LINKS</span></span>
