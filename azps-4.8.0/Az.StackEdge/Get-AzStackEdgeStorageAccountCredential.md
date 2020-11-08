---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/get-azstackedgestorageaccountcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Get-AzStackEdgeStorageAccountCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Get-AzStackEdgeStorageAccountCredential.md
ms.openlocfilehash: f198db6a49e1f5165dcfcd4effd91106cc0df831
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94243835"
---
# <span data-ttu-id="a7bf9-101">Get-AzStackEdgeStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="a7bf9-101">Get-AzStackEdgeStorageAccountCredential</span></span>

## <span data-ttu-id="a7bf9-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="a7bf9-102">SYNOPSIS</span></span>
<span data-ttu-id="a7bf9-103">Возвращает учетные данные учетной записи хранения, соответствующие учетной записи хранения на устройстве.</span><span class="sxs-lookup"><span data-stu-id="a7bf9-103">Gets the storage account credentials corresponding to the storage account on the device.</span></span>

## <span data-ttu-id="a7bf9-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="a7bf9-104">SYNTAX</span></span>

### <span data-ttu-id="a7bf9-105">ListParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="a7bf9-105">ListParameterSet (Default)</span></span>
```
Get-AzStackEdgeStorageAccountCredential [-ResourceGroupName] <String> [-DeviceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a7bf9-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a7bf9-106">GetByResourceIdParameterSet</span></span>
```
Get-AzStackEdgeStorageAccountCredential -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="a7bf9-107">GetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="a7bf9-107">GetByNameParameterSet</span></span>
```
Get-AzStackEdgeStorageAccountCredential [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a7bf9-108">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a7bf9-108">GetByParentObjectParameterSet</span></span>
```
Get-AzStackEdgeStorageAccountCredential [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>]
 -DeviceObject <PSStackEdgeDevice> [<CommonParameters>]
```

## <span data-ttu-id="a7bf9-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a7bf9-109">DESCRIPTION</span></span>
<span data-ttu-id="a7bf9-110">Командлет **Get-AzStackEdgeStorageAccountCredential** получает учетные данные учетной записи хранения для соответствующей учетной записи хранения на пограничном устройстве стека.</span><span class="sxs-lookup"><span data-stu-id="a7bf9-110">The **Get-AzStackEdgeStorageAccountCredential** cmdlet gets the storage account credentials for the corresponding storage account on the Stack Edge device.</span></span> <span data-ttu-id="a7bf9-111">Вы можете задать имя, имя группы ресурсов и параметры имени устройства, чтобы получить сведения о конкретных данных учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="a7bf9-111">You can specify Name, Resource Group Name and Device Name parameters to get information about a specific storage account credential.</span></span>

## <span data-ttu-id="a7bf9-112">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="a7bf9-112">EXAMPLES</span></span>

### <span data-ttu-id="a7bf9-113">Пример 1</span><span class="sxs-lookup"><span data-stu-id="a7bf9-113">Example 1</span></span>
```powershell
PS C:\>  Get-AzStackEdgeStorageAccountCredential -ResourceGroupName resourceGroupName -DeviceName deviceName
Name                          StorageAccount          SslStatus  ResourceGroupName
----------------------------- ---------------------- ---------- ---------------------
storageAccountCredentialName  StorageAccountName     Enabled    resourceGroupName
```

## <span data-ttu-id="a7bf9-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="a7bf9-114">PARAMETERS</span></span>

### <span data-ttu-id="a7bf9-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a7bf9-115">-DefaultProfile</span></span>
<span data-ttu-id="a7bf9-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="a7bf9-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a7bf9-117">-Имя_устройства</span><span class="sxs-lookup"><span data-stu-id="a7bf9-117">-DeviceName</span></span>
<span data-ttu-id="a7bf9-118">Имя устройства</span><span class="sxs-lookup"><span data-stu-id="a7bf9-118">Device Name</span></span>

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

### <span data-ttu-id="a7bf9-119">-DeviceObject</span><span class="sxs-lookup"><span data-stu-id="a7bf9-119">-DeviceObject</span></span>
<span data-ttu-id="a7bf9-120">Укажите соответствующий объект устройства</span><span class="sxs-lookup"><span data-stu-id="a7bf9-120">Please provide corresponding device object</span></span>

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

### <span data-ttu-id="a7bf9-121">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="a7bf9-121">-Name</span></span>
<span data-ttu-id="a7bf9-122">Имя учетной записи хранения, которую нужно использовать</span><span class="sxs-lookup"><span data-stu-id="a7bf9-122">Name of the storage account to be used</span></span>

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

### <span data-ttu-id="a7bf9-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a7bf9-123">-ResourceGroupName</span></span>
<span data-ttu-id="a7bf9-124">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="a7bf9-124">Resource Group Name</span></span>

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

### <span data-ttu-id="a7bf9-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a7bf9-125">-ResourceId</span></span>
<span data-ttu-id="a7bf9-126">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="a7bf9-126">Azure ResourceId</span></span>

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

### <span data-ttu-id="a7bf9-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a7bf9-127">CommonParameters</span></span>
<span data-ttu-id="a7bf9-128">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="a7bf9-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a7bf9-129">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a7bf9-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a7bf9-130">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="a7bf9-130">INPUTS</span></span>

### <span data-ttu-id="a7bf9-131">Microsoft. Azure. PowerShell. командлеты. StackEdge. Models. PSStackEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="a7bf9-131">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeDevice</span></span>

## <span data-ttu-id="a7bf9-132">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="a7bf9-132">OUTPUTS</span></span>

### <span data-ttu-id="a7bf9-133">Microsoft. Azure. PowerShell. командлеты. StackEdge. Models. PSStackEdgeStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="a7bf9-133">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeStorageAccountCredential</span></span>

## <span data-ttu-id="a7bf9-134">Пуск</span><span class="sxs-lookup"><span data-stu-id="a7bf9-134">NOTES</span></span>

## <span data-ttu-id="a7bf9-135">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a7bf9-135">RELATED LINKS</span></span>
