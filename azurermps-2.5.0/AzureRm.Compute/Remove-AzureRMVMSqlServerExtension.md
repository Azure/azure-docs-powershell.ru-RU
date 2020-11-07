---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: B02CEAC8-C838-4890-8C21-9897CA39EF45
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/remove-azurermvmsqlserverextension
schema: 2.0.0
ms.openlocfilehash: aa37745469ad6610fa2511d49c3404bbf54d8059
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93914558"
---
# <span data-ttu-id="93678-101">Remove-AzureRmVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="93678-101">Remove-AzureRmVMSqlServerExtension</span></span>

## <span data-ttu-id="93678-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="93678-102">SYNOPSIS</span></span>
<span data-ttu-id="93678-103">Удаляет расширение SQL Server из виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="93678-103">Removes a SQL Server extension from a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="93678-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="93678-104">SYNTAX</span></span>

```
Remove-AzureRmVMSqlServerExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="93678-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="93678-105">DESCRIPTION</span></span>
<span data-ttu-id="93678-106">Командлет **Remove-AzureRmVMSqlServerExtension** удаляет расширение сервера AzureSQL из виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="93678-106">The **Remove-AzureRmVMSqlServerExtension** cmdlet removes an AzureSQL Server extension from a virtual machine.</span></span>

## <span data-ttu-id="93678-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="93678-107">EXAMPLES</span></span>

### <span data-ttu-id="93678-108">Пример 1: удаление расширения SQL Server</span><span class="sxs-lookup"><span data-stu-id="93678-108">Example 1: Remove a SQL Server extension</span></span>
```
PS C:\> Remove-AzureRMVMSqlServerExtension -ResourceGroupName "ResourceGroup11" -VMName "ContosoVM22" -Name "SqlIaaSAgent"
```

<span data-ttu-id="93678-109">Эта команда удаляет расширение SQL Server из виртуальной машины с именем ContosoVM22.</span><span class="sxs-lookup"><span data-stu-id="93678-109">This command removes a SQL Server extension from the virtual machine named ContosoVM22.</span></span>

## <span data-ttu-id="93678-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="93678-110">PARAMETERS</span></span>

### <span data-ttu-id="93678-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="93678-111">-DefaultProfile</span></span>
<span data-ttu-id="93678-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="93678-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="93678-113">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="93678-113">-Name</span></span>
<span data-ttu-id="93678-114">Указывает имя сервера SQL Server, расширение которого удаляется этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="93678-114">Specifies the name of the SQL Server the extension that this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ExtensionName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="93678-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="93678-115">-ResourceGroupName</span></span>
<span data-ttu-id="93678-116">Указывает имя группы ресурсов виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="93678-116">Specifies the name of the resource group of the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="93678-117">-VMName</span><span class="sxs-lookup"><span data-stu-id="93678-117">-VMName</span></span>
<span data-ttu-id="93678-118">Указывает имя виртуальной машины, с помощью которой этот командлет удаляет расширение SQL Server.</span><span class="sxs-lookup"><span data-stu-id="93678-118">Specifies the name of the virtual machine from which this cmdlet removes the SQL Server extension.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="93678-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="93678-119">CommonParameters</span></span>
<span data-ttu-id="93678-120">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="93678-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="93678-121">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="93678-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="93678-122">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="93678-122">INPUTS</span></span>

### <span data-ttu-id="93678-123">Ничего</span><span class="sxs-lookup"><span data-stu-id="93678-123">None</span></span>
<span data-ttu-id="93678-124">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="93678-124">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="93678-125">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="93678-125">OUTPUTS</span></span>

### <span data-ttu-id="93678-126">Microsoft. Azure. Commands. COMPUTE. Models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="93678-126">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="93678-127">Пуск</span><span class="sxs-lookup"><span data-stu-id="93678-127">NOTES</span></span>

## <span data-ttu-id="93678-128">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="93678-128">RELATED LINKS</span></span>

[<span data-ttu-id="93678-129">Get-AzureRmVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="93678-129">Get-AzureRmVMSqlServerExtension</span></span>](./Get-AzureRMVMSqlServerExtension.md)

[<span data-ttu-id="93678-130">Set-AzureRmVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="93678-130">Set-AzureRmVMSqlServerExtension</span></span>](./Set-AzureRMVMSqlServerExtension.md)


