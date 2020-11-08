---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SqlVirtualMachine.dll-Help.xml
Module Name: Az.SqlVirtualMachine
online version: https://docs.microsoft.com/en-us/powershell/module/az.sqlvirtualmachine/get-azsqlvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/Get-AzSqlVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/Get-AzSqlVM.md
ms.openlocfilehash: b6f5b885e2cb65c8cf4775f8bb37742b8d98b6a3
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94243845"
---
# <span data-ttu-id="f5ddf-101">Get-AzSqlVM</span><span class="sxs-lookup"><span data-stu-id="f5ddf-101">Get-AzSqlVM</span></span>

## <span data-ttu-id="f5ddf-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="f5ddf-102">SYNOPSIS</span></span>
<span data-ttu-id="f5ddf-103">Получает одну или несколько виртуальных машин SQL.</span><span class="sxs-lookup"><span data-stu-id="f5ddf-103">Gets one or more sql virtual machines.</span></span>

## <span data-ttu-id="f5ddf-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="f5ddf-104">SYNTAX</span></span>

### <span data-ttu-id="f5ddf-105">ResourceGroupOnly (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="f5ddf-105">ResourceGroupOnly (Default)</span></span>
```
Get-AzSqlVM [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f5ddf-106">Псевдоним</span><span class="sxs-lookup"><span data-stu-id="f5ddf-106">Name</span></span>
```
Get-AzSqlVM [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="f5ddf-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="f5ddf-107">ResourceId</span></span>
```
Get-AzSqlVM [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f5ddf-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f5ddf-108">DESCRIPTION</span></span>
<span data-ttu-id="f5ddf-109">Командлет Get-AzSqlVM получает одну или несколько виртуальных машин SQL.</span><span class="sxs-lookup"><span data-stu-id="f5ddf-109">The Get-AzSqlVM cmdlet gets one or more sql virtual machines.</span></span>

## <span data-ttu-id="f5ddf-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="f5ddf-110">EXAMPLES</span></span>

### <span data-ttu-id="f5ddf-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="f5ddf-111">Example 1</span></span>
```powershell
PS C:\> Get-AzSqlVM

Name ResourceGroupName  LicenseType Sku       Offer          SqlManagementType
---- -----------------  ----------- ---       -----          -----------------
vm   ResourceGroup01    PAYG        Developer SQL2017-WS2016 Full
vm2  ResourceGroup02    PAYG        Developer SQL2017-WS2016 Full
```

<span data-ttu-id="f5ddf-112">Эта команда получает сведения обо всех виртуальных машинах Azure SQL в текущей подписке.</span><span class="sxs-lookup"><span data-stu-id="f5ddf-112">This command gets information about all the Azure SQL virtual machines in the current subscription.</span></span>

### <span data-ttu-id="f5ddf-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="f5ddf-113">Example 2</span></span>
```powershell
PS C:\> Get-AzSqlVM -ResourceGroupName "ResourceGroup01"
Name ResourceGroupName  LicenseType Sku       Offer          SqlManagementType
---- -----------------  ----------- ---       -----          -----------------
vm   ResourceGroup01    PAYG        Developer SQL2017-WS2016 Full
```

<span data-ttu-id="f5ddf-114">Эта команда получает сведения обо всех виртуальных машинах Azure SQL в текущей подписке, назначенной группе ресурсов ResourceGroup01.</span><span class="sxs-lookup"><span data-stu-id="f5ddf-114">This command gets information about all the Azure SQL virtual machines in the current subscription assigned to the resource group ResourceGroup01.</span></span>

### <span data-ttu-id="f5ddf-115">Пример 3</span><span class="sxs-lookup"><span data-stu-id="f5ddf-115">Example 3</span></span>
```powershell
PS C:\> Get-AzSqlVM -ResourceGroupName "ResourceGroup01" -Name "vm"
Name ResourceGroupName  LicenseType Sku       Offer          SqlManagementType
---- -----------------  ----------- ---       -----          -----------------
vm   ResourceGroup01    PAYG        Developer SQL2017-WS2016 Full
```

<span data-ttu-id="f5ddf-116">Эта команда получает сведения о виртуальной машине SQL "VM", назначенной группе ресурсов ResourceGroup01.</span><span class="sxs-lookup"><span data-stu-id="f5ddf-116">This command gets information about the SQL virtual machine "vm" assigned to the resource group ResourceGroup01.</span></span>

## <span data-ttu-id="f5ddf-117">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="f5ddf-117">PARAMETERS</span></span>

### <span data-ttu-id="f5ddf-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f5ddf-118">-DefaultProfile</span></span>
<span data-ttu-id="f5ddf-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="f5ddf-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f5ddf-120">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="f5ddf-120">-Name</span></span>
<span data-ttu-id="f5ddf-121">Имя виртуальной машины SQL.</span><span class="sxs-lookup"><span data-stu-id="f5ddf-121">SQL virtual machine name.</span></span>

```yaml
Type: System.String
Parameter Sets: Name
Aliases: SqlVMName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f5ddf-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f5ddf-122">-ResourceGroupName</span></span>
<span data-ttu-id="f5ddf-123">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="f5ddf-123">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupOnly
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: Name
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f5ddf-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f5ddf-124">-ResourceId</span></span>
<span data-ttu-id="f5ddf-125">Идентификатор ресурса виртуальной машины SQL.</span><span class="sxs-lookup"><span data-stu-id="f5ddf-125">SQL virtual machine resource id.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceId
Aliases: SqlVMId

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f5ddf-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f5ddf-126">CommonParameters</span></span>
<span data-ttu-id="f5ddf-127">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="f5ddf-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f5ddf-128">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f5ddf-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f5ddf-129">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="f5ddf-129">INPUTS</span></span>

### <span data-ttu-id="f5ddf-130">Ничего</span><span class="sxs-lookup"><span data-stu-id="f5ddf-130">None</span></span>

## <span data-ttu-id="f5ddf-131">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="f5ddf-131">OUTPUTS</span></span>

### <span data-ttu-id="f5ddf-132">Microsoft. Azure. Commands. SqlVirtualMachine. SqlVirtualMachine. Model. AzureSqlVMModel</span><span class="sxs-lookup"><span data-stu-id="f5ddf-132">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMModel</span></span>

## <span data-ttu-id="f5ddf-133">Пуск</span><span class="sxs-lookup"><span data-stu-id="f5ddf-133">NOTES</span></span>

## <span data-ttu-id="f5ddf-134">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f5ddf-134">RELATED LINKS</span></span>
