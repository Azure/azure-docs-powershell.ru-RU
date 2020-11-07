---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SqlVirtualMachine.dll-Help.xml
Module Name: Az.SqlVirtualMachine
online version: https://docs.microsoft.com/en-us/powershell/module/az.sqlvirtualmachine/get-azsqlvmgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/Get-AzSqlVMGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/Get-AzSqlVMGroup.md
ms.openlocfilehash: fc4a0624b6e5702c0ef0c836f0b6ac593c25dafe
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "93912435"
---
# <span data-ttu-id="ee07f-101">Get-AzSqlVMGroup</span><span class="sxs-lookup"><span data-stu-id="ee07f-101">Get-AzSqlVMGroup</span></span>

## <span data-ttu-id="ee07f-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="ee07f-102">SYNOPSIS</span></span>
<span data-ttu-id="ee07f-103">Возвращает одну или несколько групп виртуальных машин SQL.</span><span class="sxs-lookup"><span data-stu-id="ee07f-103">Gets one or more sql virtual machine groups.</span></span>

## <span data-ttu-id="ee07f-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="ee07f-104">SYNTAX</span></span>

### <span data-ttu-id="ee07f-105">ResourceGroupOnly (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="ee07f-105">ResourceGroupOnly (Default)</span></span>
```
Get-AzSqlVMGroup [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="ee07f-106">Псевдоним</span><span class="sxs-lookup"><span data-stu-id="ee07f-106">Name</span></span>
```
Get-AzSqlVMGroup [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="ee07f-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="ee07f-107">ResourceId</span></span>
```
Get-AzSqlVMGroup [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ee07f-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ee07f-108">DESCRIPTION</span></span>
<span data-ttu-id="ee07f-109">Командлет Get-AzSqlVMGroup получает одну или несколько групп виртуальных машин SQL.</span><span class="sxs-lookup"><span data-stu-id="ee07f-109">The Get-AzSqlVMGroup cmdlet gets one or more sql virtual machine groups.</span></span>

## <span data-ttu-id="ee07f-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="ee07f-110">EXAMPLES</span></span>

### <span data-ttu-id="ee07f-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="ee07f-111">Example 1</span></span>
```powershell
PS C:\> Get-AzSqlVMGroup

Name       ResourceGroupName  Sku       Offer
----       -----------------  ---       -----
test-group ResourceGroup01    Developer SQL2017-WS2016
group1     ResourceGroup02    Developer SQL2017-WS2016
```

<span data-ttu-id="ee07f-112">Эта команда получает сведения обо всех группах виртуальных машин Azure SQL в текущей подписке.</span><span class="sxs-lookup"><span data-stu-id="ee07f-112">This command gets information about all the Azure SQL virtual machine groups in the current subscription.</span></span>

### <span data-ttu-id="ee07f-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="ee07f-113">Example 2</span></span>
```powershell
PS C:\> Get-AzSqlVMGroup -ResourceGroupName "ResourceGroup01"
Name       ResourceGroupName  Sku       Offer
----       -----------------  ---       -----
test-group ResourceGroup01    Developer SQL2017-WS2016
```

<span data-ttu-id="ee07f-114">Эта команда получает сведения обо всех группах виртуальных машин SQL для Azure в текущей подписке, назначенной группе ресурсов ResourceGroup01.</span><span class="sxs-lookup"><span data-stu-id="ee07f-114">This command gets information about all the Azure SQL virtual machine groups in the current subscription assigned to the resource group ResourceGroup01.</span></span>

### <span data-ttu-id="ee07f-115">Пример 3</span><span class="sxs-lookup"><span data-stu-id="ee07f-115">Example 3</span></span>
```powershell
PS C:\> Get-AzSqlVMGroup -ResourceGroupName "ResourceGroup01" -Name "test-group"
Name       ResourceGroupName  Sku       Offer
----       -----------------  ---       -----
test-group ResourceGroup01    Developer SQL2017-WS2016
```

<span data-ttu-id="ee07f-116">Эта команда получает сведения о группе "тест-ResourceGroup01" в SQL, назначенной группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="ee07f-116">This command gets information about the SQL virtual machine group "test-group" assigned to the resource group ResourceGroup01.</span></span>

## <span data-ttu-id="ee07f-117">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="ee07f-117">PARAMETERS</span></span>

### <span data-ttu-id="ee07f-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ee07f-118">-DefaultProfile</span></span>
<span data-ttu-id="ee07f-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="ee07f-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ee07f-120">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="ee07f-120">-Name</span></span>
<span data-ttu-id="ee07f-121">Имя группы виртуальной машины SQL.</span><span class="sxs-lookup"><span data-stu-id="ee07f-121">SQL virtual machine group name.</span></span>

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

### <span data-ttu-id="ee07f-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ee07f-122">-ResourceGroupName</span></span>
<span data-ttu-id="ee07f-123">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="ee07f-123">The name of the resource group.</span></span>

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

### <span data-ttu-id="ee07f-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ee07f-124">-ResourceId</span></span>
<span data-ttu-id="ee07f-125">Идентификатор ресурса группы виртуальной машины SQL.</span><span class="sxs-lookup"><span data-stu-id="ee07f-125">SQL virtual machine group resource id.</span></span>

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

### <span data-ttu-id="ee07f-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ee07f-126">CommonParameters</span></span>
<span data-ttu-id="ee07f-127">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="ee07f-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ee07f-128">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ee07f-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ee07f-129">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="ee07f-129">INPUTS</span></span>

### <span data-ttu-id="ee07f-130">System. String</span><span class="sxs-lookup"><span data-stu-id="ee07f-130">System.String</span></span>

## <span data-ttu-id="ee07f-131">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="ee07f-131">OUTPUTS</span></span>

### <span data-ttu-id="ee07f-132">Microsoft. Azure. Commands. SqlVirtualMachine. SqlVirtualMachine. Model. AzureSqlVMGroupModel</span><span class="sxs-lookup"><span data-stu-id="ee07f-132">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMGroupModel</span></span>

## <span data-ttu-id="ee07f-133">Пуск</span><span class="sxs-lookup"><span data-stu-id="ee07f-133">NOTES</span></span>

## <span data-ttu-id="ee07f-134">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ee07f-134">RELATED LINKS</span></span>
