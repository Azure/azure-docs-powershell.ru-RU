---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SqlVirtualMachine.dll-Help.xml
Module Name: Az.SqlVirtualMachine
online version: https://docs.microsoft.com/en-us/powershell/module/az.sqlvirtualmachine/new-azsqlvmconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/New-AzSqlVMConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/New-AzSqlVMConfig.md
ms.openlocfilehash: 0f914ab2f5c39cd53239302b2f0acd12a3e13133
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94246946"
---
# <span data-ttu-id="c99ca-101">New-AzSqlVMConfig</span><span class="sxs-lookup"><span data-stu-id="c99ca-101">New-AzSqlVMConfig</span></span>

## <span data-ttu-id="c99ca-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="c99ca-102">SYNOPSIS</span></span>
<span data-ttu-id="c99ca-103">Создание новой конфигурации для виртуальной машины SQL.</span><span class="sxs-lookup"><span data-stu-id="c99ca-103">Creates a new configuration for a sql virtual machine.</span></span>

## <span data-ttu-id="c99ca-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="c99ca-104">SYNTAX</span></span>

```
New-AzSqlVMConfig [-LicenseType] <String> [-Offer <String>] [-Sku <String>] [-SqlManagementType <String>]
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c99ca-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c99ca-105">DESCRIPTION</span></span>
<span data-ttu-id="c99ca-106">Командлет New-AzSqlVMConfig создает новый объект конфигурации для виртуальной машины SQL.</span><span class="sxs-lookup"><span data-stu-id="c99ca-106">The New-AzSqlVMConfig cmdlet creates a new configuration object for a sql virtual machine.</span></span>

## <span data-ttu-id="c99ca-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="c99ca-107">EXAMPLES</span></span>

### <span data-ttu-id="c99ca-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="c99ca-108">Example 1</span></span>
```powershell
PS C:\> $config = New-AzSqlVMConfig -LicenseType "PAYG"
PS C:\> New-AzSqlVM -ResourceGroupName "ResourceGroup01" -Name "vm" -SqlVM $config
Name ResourceGroupName  LicenseType Sku       Offer          SqlManagementType
---- -----------------  ----------- ---       -----          -----------------
vm   ResourceGroup01    PAYG        Developer SQL2017-WS2016 Full
```

<span data-ttu-id="c99ca-109">Создание локального настраиваемого объекта виртуальной машины SQL, который можно использовать для создания виртуальной машины Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="c99ca-109">Creates a local configurable object of sql virtual machine that can be used in order to create an Azure sql virtual machine.</span></span>

## <span data-ttu-id="c99ca-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="c99ca-110">PARAMETERS</span></span>

### <span data-ttu-id="c99ca-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c99ca-111">-DefaultProfile</span></span>
<span data-ttu-id="c99ca-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="c99ca-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c99ca-113">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="c99ca-113">-LicenseType</span></span>
<span data-ttu-id="c99ca-114">Тип лицензии виртуальной машины SQL.</span><span class="sxs-lookup"><span data-stu-id="c99ca-114">SQL virtual machine license type.</span></span>

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

### <span data-ttu-id="c99ca-115">-Предложение</span><span class="sxs-lookup"><span data-stu-id="c99ca-115">-Offer</span></span>
<span data-ttu-id="c99ca-116">Предложение виртуальной машины SQL.</span><span class="sxs-lookup"><span data-stu-id="c99ca-116">SQL virtual machine offer.</span></span>

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

### <span data-ttu-id="c99ca-117">-SKU</span><span class="sxs-lookup"><span data-stu-id="c99ca-117">-Sku</span></span>
<span data-ttu-id="c99ca-118">Тип выпусков виртуальной машины SQL.</span><span class="sxs-lookup"><span data-stu-id="c99ca-118">SQL virtual machine edition type.</span></span>

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

### <span data-ttu-id="c99ca-119">-SqlManagementType</span><span class="sxs-lookup"><span data-stu-id="c99ca-119">-SqlManagementType</span></span>
<span data-ttu-id="c99ca-120">Тип управления виртуальными машинами SQL.</span><span class="sxs-lookup"><span data-stu-id="c99ca-120">SQL virtual machine management type.</span></span>

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

### <span data-ttu-id="c99ca-121">-Тег</span><span class="sxs-lookup"><span data-stu-id="c99ca-121">-Tag</span></span>
<span data-ttu-id="c99ca-122">Теги, связываемые с виртуальной машиной SQL</span><span class="sxs-lookup"><span data-stu-id="c99ca-122">The tags to associate with the SQL virtual machine</span></span>

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

### <span data-ttu-id="c99ca-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c99ca-123">CommonParameters</span></span>
<span data-ttu-id="c99ca-124">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="c99ca-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c99ca-125">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c99ca-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c99ca-126">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="c99ca-126">INPUTS</span></span>

### <span data-ttu-id="c99ca-127">Ничего</span><span class="sxs-lookup"><span data-stu-id="c99ca-127">None</span></span>

## <span data-ttu-id="c99ca-128">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="c99ca-128">OUTPUTS</span></span>

### <span data-ttu-id="c99ca-129">Microsoft. Azure. Commands. SqlVirtualMachine. SqlVirtualMachine. Model. AzureSqlVMModel</span><span class="sxs-lookup"><span data-stu-id="c99ca-129">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMModel</span></span>

## <span data-ttu-id="c99ca-130">Пуск</span><span class="sxs-lookup"><span data-stu-id="c99ca-130">NOTES</span></span>

## <span data-ttu-id="c99ca-131">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c99ca-131">RELATED LINKS</span></span>