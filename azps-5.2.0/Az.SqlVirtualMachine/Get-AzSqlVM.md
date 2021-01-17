---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SqlVirtualMachine.dll-Help.xml
Module Name: Az.SqlVirtualMachine
online version: https://docs.microsoft.com/en-us/powershell/module/az.sqlvirtualmachine/get-azsqlvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/Get-AzSqlVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/Get-AzSqlVM.md
ms.openlocfilehash: b6f5b885e2cb65c8cf4775f8bb37742b8d98b6a3
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98413452"
---
# <span data-ttu-id="f5141-101">Get-AzSqlVM</span><span class="sxs-lookup"><span data-stu-id="f5141-101">Get-AzSqlVM</span></span>

## <span data-ttu-id="f5141-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f5141-102">SYNOPSIS</span></span>
<span data-ttu-id="f5141-103">Возвращает одну или несколько виртуальных машин SQL.</span><span class="sxs-lookup"><span data-stu-id="f5141-103">Gets one or more sql virtual machines.</span></span>

## <span data-ttu-id="f5141-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="f5141-104">SYNTAX</span></span>

### <span data-ttu-id="f5141-105">ResourceGroupOnly (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="f5141-105">ResourceGroupOnly (Default)</span></span>
```
Get-AzSqlVM [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f5141-106">Имя</span><span class="sxs-lookup"><span data-stu-id="f5141-106">Name</span></span>
```
Get-AzSqlVM [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="f5141-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="f5141-107">ResourceId</span></span>
```
Get-AzSqlVM [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f5141-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f5141-108">DESCRIPTION</span></span>
<span data-ttu-id="f5141-109">Этот Get-AzSqlVM получает одну или несколько виртуальных машин SQL.</span><span class="sxs-lookup"><span data-stu-id="f5141-109">The Get-AzSqlVM cmdlet gets one or more sql virtual machines.</span></span>

## <span data-ttu-id="f5141-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="f5141-110">EXAMPLES</span></span>

### <span data-ttu-id="f5141-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="f5141-111">Example 1</span></span>
```powershell
PS C:\> Get-AzSqlVM

Name ResourceGroupName  LicenseType Sku       Offer          SqlManagementType
---- -----------------  ----------- ---       -----          -----------------
vm   ResourceGroup01    PAYG        Developer SQL2017-WS2016 Full
vm2  ResourceGroup02    PAYG        Developer SQL2017-WS2016 Full
```

<span data-ttu-id="f5141-112">Эта команда получает сведения обо всех виртуальных машинах Azure SQL в текущей подписке.</span><span class="sxs-lookup"><span data-stu-id="f5141-112">This command gets information about all the Azure SQL virtual machines in the current subscription.</span></span>

### <span data-ttu-id="f5141-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="f5141-113">Example 2</span></span>
```powershell
PS C:\> Get-AzSqlVM -ResourceGroupName "ResourceGroup01"
Name ResourceGroupName  LicenseType Sku       Offer          SqlManagementType
---- -----------------  ----------- ---       -----          -----------------
vm   ResourceGroup01    PAYG        Developer SQL2017-WS2016 Full
```

<span data-ttu-id="f5141-114">Эта команда получает сведения обо всех виртуальных машинах Azure SQL в текущей подписке, назначенной группе ресурсов ResourceGroup01.</span><span class="sxs-lookup"><span data-stu-id="f5141-114">This command gets information about all the Azure SQL virtual machines in the current subscription assigned to the resource group ResourceGroup01.</span></span>

### <span data-ttu-id="f5141-115">Пример 3</span><span class="sxs-lookup"><span data-stu-id="f5141-115">Example 3</span></span>
```powershell
PS C:\> Get-AzSqlVM -ResourceGroupName "ResourceGroup01" -Name "vm"
Name ResourceGroupName  LicenseType Sku       Offer          SqlManagementType
---- -----------------  ----------- ---       -----          -----------------
vm   ResourceGroup01    PAYG        Developer SQL2017-WS2016 Full
```

<span data-ttu-id="f5141-116">Эта команда получает сведения о SQL "vm", назначенной группе ресурсов ResourceGroup01.</span><span class="sxs-lookup"><span data-stu-id="f5141-116">This command gets information about the SQL virtual machine "vm" assigned to the resource group ResourceGroup01.</span></span>

## <span data-ttu-id="f5141-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f5141-117">PARAMETERS</span></span>

### <span data-ttu-id="f5141-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f5141-118">-DefaultProfile</span></span>
<span data-ttu-id="f5141-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="f5141-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f5141-120">-Name</span><span class="sxs-lookup"><span data-stu-id="f5141-120">-Name</span></span>
<span data-ttu-id="f5141-121">SQL имя виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="f5141-121">SQL virtual machine name.</span></span>

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

### <span data-ttu-id="f5141-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f5141-122">-ResourceGroupName</span></span>
<span data-ttu-id="f5141-123">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="f5141-123">The name of the resource group.</span></span>

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

### <span data-ttu-id="f5141-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f5141-124">-ResourceId</span></span>
<span data-ttu-id="f5141-125">SQL виртуальных машинных ресурсов.</span><span class="sxs-lookup"><span data-stu-id="f5141-125">SQL virtual machine resource id.</span></span>

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

### <span data-ttu-id="f5141-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f5141-126">CommonParameters</span></span>
<span data-ttu-id="f5141-127">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f5141-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f5141-128">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f5141-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f5141-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="f5141-129">INPUTS</span></span>

### <span data-ttu-id="f5141-130">Нет</span><span class="sxs-lookup"><span data-stu-id="f5141-130">None</span></span>

## <span data-ttu-id="f5141-131">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="f5141-131">OUTPUTS</span></span>

### <span data-ttu-id="f5141-132">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMavire.Model.AzureSqlVMModel</span><span class="sxs-lookup"><span data-stu-id="f5141-132">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMModel</span></span>

## <span data-ttu-id="f5141-133">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="f5141-133">NOTES</span></span>

## <span data-ttu-id="f5141-134">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f5141-134">RELATED LINKS</span></span>
