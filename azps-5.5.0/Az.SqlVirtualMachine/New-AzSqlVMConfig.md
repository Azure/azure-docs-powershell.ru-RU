---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SqlVirtualMachine.dll-Help.xml
Module Name: Az.SqlVirtualMachine
online version: https://docs.microsoft.com/en-us/powershell/module/az.sqlvirtualmachine/new-azsqlvmconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/New-AzSqlVMConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/New-AzSqlVMConfig.md
ms.openlocfilehash: 0f914ab2f5c39cd53239302b2f0acd12a3e13133
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100241909"
---
# <span data-ttu-id="695e2-101">New-AzSqlVMConfig</span><span class="sxs-lookup"><span data-stu-id="695e2-101">New-AzSqlVMConfig</span></span>

## <span data-ttu-id="695e2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="695e2-102">SYNOPSIS</span></span>
<span data-ttu-id="695e2-103">Создает новую конфигурацию виртуальной машины SQL.</span><span class="sxs-lookup"><span data-stu-id="695e2-103">Creates a new configuration for a sql virtual machine.</span></span>

## <span data-ttu-id="695e2-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="695e2-104">SYNTAX</span></span>

```
New-AzSqlVMConfig [-LicenseType] <String> [-Offer <String>] [-Sku <String>] [-SqlManagementType <String>]
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="695e2-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="695e2-105">DESCRIPTION</span></span>
<span data-ttu-id="695e2-106">С New-AzSqlVMConfig-технологией создается новый объект конфигурации для виртуальной машины SQL.</span><span class="sxs-lookup"><span data-stu-id="695e2-106">The New-AzSqlVMConfig cmdlet creates a new configuration object for a sql virtual machine.</span></span>

## <span data-ttu-id="695e2-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="695e2-107">EXAMPLES</span></span>

### <span data-ttu-id="695e2-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="695e2-108">Example 1</span></span>
```powershell
PS C:\> $config = New-AzSqlVMConfig -LicenseType "PAYG"
PS C:\> New-AzSqlVM -ResourceGroupName "ResourceGroup01" -Name "vm" -SqlVM $config
Name ResourceGroupName  LicenseType Sku       Offer          SqlManagementType
---- -----------------  ----------- ---       -----          -----------------
vm   ResourceGroup01    PAYG        Developer SQL2017-WS2016 Full
```

<span data-ttu-id="695e2-109">Создает локальный настраиваемый объект виртуальной машины SQL, который можно использовать для создания виртуальной машины SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="695e2-109">Creates a local configurable object of sql virtual machine that can be used in order to create an Azure sql virtual machine.</span></span>

## <span data-ttu-id="695e2-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="695e2-110">PARAMETERS</span></span>

### <span data-ttu-id="695e2-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="695e2-111">-DefaultProfile</span></span>
<span data-ttu-id="695e2-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="695e2-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="695e2-113">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="695e2-113">-LicenseType</span></span>
<span data-ttu-id="695e2-114">SQL тип лицензии виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="695e2-114">SQL virtual machine license type.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="695e2-115">-Offer</span><span class="sxs-lookup"><span data-stu-id="695e2-115">-Offer</span></span>
<span data-ttu-id="695e2-116">SQL виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="695e2-116">SQL virtual machine offer.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="695e2-117">-SKU</span><span class="sxs-lookup"><span data-stu-id="695e2-117">-Sku</span></span>
<span data-ttu-id="695e2-118">SQL выпуска виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="695e2-118">SQL virtual machine edition type.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="695e2-119">-SqlManagementType</span><span class="sxs-lookup"><span data-stu-id="695e2-119">-SqlManagementType</span></span>
<span data-ttu-id="695e2-120">SQL типа управления виртуальными компьютерами.</span><span class="sxs-lookup"><span data-stu-id="695e2-120">SQL virtual machine management type.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="695e2-121">-Tag</span><span class="sxs-lookup"><span data-stu-id="695e2-121">-Tag</span></span>
<span data-ttu-id="695e2-122">Теги, которые нужно связать с виртуальной SQL компьютера</span><span class="sxs-lookup"><span data-stu-id="695e2-122">The tags to associate with the SQL virtual machine</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="695e2-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="695e2-123">CommonParameters</span></span>
<span data-ttu-id="695e2-124">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="695e2-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="695e2-125">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="695e2-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="695e2-126">INPUTS</span><span class="sxs-lookup"><span data-stu-id="695e2-126">INPUTS</span></span>

### <span data-ttu-id="695e2-127">Нет</span><span class="sxs-lookup"><span data-stu-id="695e2-127">None</span></span>

## <span data-ttu-id="695e2-128">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="695e2-128">OUTPUTS</span></span>

### <span data-ttu-id="695e2-129">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMavire.Model.AzureSqlVMModel</span><span class="sxs-lookup"><span data-stu-id="695e2-129">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMModel</span></span>

## <span data-ttu-id="695e2-130">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="695e2-130">NOTES</span></span>

## <span data-ttu-id="695e2-131">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="695e2-131">RELATED LINKS</span></span>
