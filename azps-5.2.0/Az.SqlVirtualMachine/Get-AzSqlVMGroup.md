---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SqlVirtualMachine.dll-Help.xml
Module Name: Az.SqlVirtualMachine
online version: https://docs.microsoft.com/en-us/powershell/module/az.sqlvirtualmachine/get-azsqlvmgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/Get-AzSqlVMGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/Get-AzSqlVMGroup.md
ms.openlocfilehash: fc4a0624b6e5702c0ef0c836f0b6ac593c25dafe
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98413436"
---
# <span data-ttu-id="c4529-101">Get-AzSqlVMGroup</span><span class="sxs-lookup"><span data-stu-id="c4529-101">Get-AzSqlVMGroup</span></span>

## <span data-ttu-id="c4529-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c4529-102">SYNOPSIS</span></span>
<span data-ttu-id="c4529-103">Возвращает одну или несколько групп виртуальных машин SQL.</span><span class="sxs-lookup"><span data-stu-id="c4529-103">Gets one or more sql virtual machine groups.</span></span>

## <span data-ttu-id="c4529-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="c4529-104">SYNTAX</span></span>

### <span data-ttu-id="c4529-105">ResourceGroupOnly (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="c4529-105">ResourceGroupOnly (Default)</span></span>
```
Get-AzSqlVMGroup [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="c4529-106">Имя</span><span class="sxs-lookup"><span data-stu-id="c4529-106">Name</span></span>
```
Get-AzSqlVMGroup [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="c4529-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="c4529-107">ResourceId</span></span>
```
Get-AzSqlVMGroup [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c4529-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c4529-108">DESCRIPTION</span></span>
<span data-ttu-id="c4529-109">Этот Get-AzSqlVMGroup получает одну или несколько групп виртуальных машин SQL.</span><span class="sxs-lookup"><span data-stu-id="c4529-109">The Get-AzSqlVMGroup cmdlet gets one or more sql virtual machine groups.</span></span>

## <span data-ttu-id="c4529-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="c4529-110">EXAMPLES</span></span>

### <span data-ttu-id="c4529-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="c4529-111">Example 1</span></span>
```powershell
PS C:\> Get-AzSqlVMGroup

Name       ResourceGroupName  Sku       Offer
----       -----------------  ---       -----
test-group ResourceGroup01    Developer SQL2017-WS2016
group1     ResourceGroup02    Developer SQL2017-WS2016
```

<span data-ttu-id="c4529-112">Эта команда получает сведения обо всех группах виртуальных машин Azure SQL в текущей подписке.</span><span class="sxs-lookup"><span data-stu-id="c4529-112">This command gets information about all the Azure SQL virtual machine groups in the current subscription.</span></span>

### <span data-ttu-id="c4529-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="c4529-113">Example 2</span></span>
```powershell
PS C:\> Get-AzSqlVMGroup -ResourceGroupName "ResourceGroup01"
Name       ResourceGroupName  Sku       Offer
----       -----------------  ---       -----
test-group ResourceGroup01    Developer SQL2017-WS2016
```

<span data-ttu-id="c4529-114">Эта команда получает сведения обо всех группах виртуальных машин Azure SQL в текущей подписке, назначенной группе ресурсов ResourceGroup01.</span><span class="sxs-lookup"><span data-stu-id="c4529-114">This command gets information about all the Azure SQL virtual machine groups in the current subscription assigned to the resource group ResourceGroup01.</span></span>

### <span data-ttu-id="c4529-115">Пример 3</span><span class="sxs-lookup"><span data-stu-id="c4529-115">Example 3</span></span>
```powershell
PS C:\> Get-AzSqlVMGroup -ResourceGroupName "ResourceGroup01" -Name "test-group"
Name       ResourceGroupName  Sku       Offer
----       -----------------  ---       -----
test-group ResourceGroup01    Developer SQL2017-WS2016
```

<span data-ttu-id="c4529-116">Эта команда получает сведения о группе SQL "test-group", назначенной группе ресурсов ResourceGroup01.</span><span class="sxs-lookup"><span data-stu-id="c4529-116">This command gets information about the SQL virtual machine group "test-group" assigned to the resource group ResourceGroup01.</span></span>

## <span data-ttu-id="c4529-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c4529-117">PARAMETERS</span></span>

### <span data-ttu-id="c4529-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c4529-118">-DefaultProfile</span></span>
<span data-ttu-id="c4529-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="c4529-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c4529-120">-Name</span><span class="sxs-lookup"><span data-stu-id="c4529-120">-Name</span></span>
<span data-ttu-id="c4529-121">SQL группы виртуальных машин.</span><span class="sxs-lookup"><span data-stu-id="c4529-121">SQL virtual machine group name.</span></span>

```yaml
Type: System.String
Parameter Sets: Name
Aliases: SqlVMGroupName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c4529-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c4529-122">-ResourceGroupName</span></span>
<span data-ttu-id="c4529-123">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="c4529-123">The name of the resource group.</span></span>

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

### <span data-ttu-id="c4529-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c4529-124">-ResourceId</span></span>
<span data-ttu-id="c4529-125">SQL ресурса группы виртуальных машин.</span><span class="sxs-lookup"><span data-stu-id="c4529-125">SQL virtual machine group resource id.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceId
Aliases: SqlVMGroupId

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c4529-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c4529-126">CommonParameters</span></span>
<span data-ttu-id="c4529-127">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c4529-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c4529-128">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c4529-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c4529-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c4529-129">INPUTS</span></span>

### <span data-ttu-id="c4529-130">System.String</span><span class="sxs-lookup"><span data-stu-id="c4529-130">System.String</span></span>

## <span data-ttu-id="c4529-131">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="c4529-131">OUTPUTS</span></span>

### <span data-ttu-id="c4529-132">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMavire.Model.AzureSqlVMGroupModel</span><span class="sxs-lookup"><span data-stu-id="c4529-132">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMGroupModel</span></span>

## <span data-ttu-id="c4529-133">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="c4529-133">NOTES</span></span>

## <span data-ttu-id="c4529-134">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c4529-134">RELATED LINKS</span></span>
