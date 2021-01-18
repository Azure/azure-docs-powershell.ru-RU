---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SqlVirtualMachine.dll-Help.xml
Module Name: Az.SqlVirtualMachine
online version: https://docs.microsoft.com/en-us/powershell/module/az.sqlvirtualmachine/set-azsqlvmconfiggroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/Set-AzSqlVMConfigGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/Set-AzSqlVMConfigGroup.md
ms.openlocfilehash: b83dc58161791009a3adfd7cbf9b0b07b3f0b5b1
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98505857"
---
# <span data-ttu-id="abcfa-101">Set-AzSqlVMConfigGroup</span><span class="sxs-lookup"><span data-stu-id="abcfa-101">Set-AzSqlVMConfigGroup</span></span>

## <span data-ttu-id="abcfa-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="abcfa-102">SYNOPSIS</span></span>
<span data-ttu-id="abcfa-103">В конфигурации виртуальной машины SQL можно настроить сведения относительно группы виртуальных машин SQL.</span><span class="sxs-lookup"><span data-stu-id="abcfa-103">Set the information relative to a sql virtual machine group in a sql virtual machine configuration.</span></span>

## <span data-ttu-id="abcfa-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="abcfa-104">SYNTAX</span></span>

```
Set-AzSqlVMConfigGroup [-SqlVM] <AzureSqlVMModel> [-SqlVMGroup] <AzureSqlVMGroupModel>
 -ClusterOperatorAccountPassword <SecureString> -SqlServiceAccountPassword <SecureString>
 [-ClusterBootstrapAccountPassword <SecureString>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="abcfa-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="abcfa-105">DESCRIPTION</span></span>
<span data-ttu-id="abcfa-106">С Set-AzSqlVMConfigGroup набор данных, необходимых для присоединиться к группе виртуальных машин SQL для конфигурации виртуальной машины SQL.</span><span class="sxs-lookup"><span data-stu-id="abcfa-106">The Set-AzSqlVMConfigGroup cmdlet set the information needed in order to join a sql virtual machine group for a sql virtual machine configuration.</span></span>

## <span data-ttu-id="abcfa-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="abcfa-107">EXAMPLES</span></span>

### <span data-ttu-id="abcfa-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="abcfa-108">Example 1</span></span>
```powershell
PS C:\> $config = Set-AzSqlVMConfigGroup -SqlVM $config -SqlVMGroup $group -ClusterOperatorAccountPassword 'password' -SqlServiceAccountPassword 'password'
```

<span data-ttu-id="abcfa-109">Обновление сведений о группе конфигурации виртуальной машины SQL.</span><span class="sxs-lookup"><span data-stu-id="abcfa-109">Update the group informations of a sql virtual machine configuration.</span></span>

## <span data-ttu-id="abcfa-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="abcfa-110">PARAMETERS</span></span>

### <span data-ttu-id="abcfa-111">-ClusterBootstrapAccountPassword</span><span class="sxs-lookup"><span data-stu-id="abcfa-111">-ClusterBootstrapAccountPassword</span></span>
<span data-ttu-id="abcfa-112">Пароль для учетной записи bootstrap кластера</span><span class="sxs-lookup"><span data-stu-id="abcfa-112">Password for the cluster bootstrap account</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="abcfa-113">-ClusterOperatorAccountPassword</span><span class="sxs-lookup"><span data-stu-id="abcfa-113">-ClusterOperatorAccountPassword</span></span>
<span data-ttu-id="abcfa-114">Пароль для учетной записи оператора кластера</span><span class="sxs-lookup"><span data-stu-id="abcfa-114">Password for the cluster operator account</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="abcfa-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="abcfa-115">-DefaultProfile</span></span>
<span data-ttu-id="abcfa-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="abcfa-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="abcfa-117">-SqlServiceAccountPassword</span><span class="sxs-lookup"><span data-stu-id="abcfa-117">-SqlServiceAccountPassword</span></span>
<span data-ttu-id="abcfa-118">Пароль для учетной SQL службы</span><span class="sxs-lookup"><span data-stu-id="abcfa-118">Password for the SQL service account</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="abcfa-119">-SqlVM</span><span class="sxs-lookup"><span data-stu-id="abcfa-119">-SqlVM</span></span>
<span data-ttu-id="abcfa-120">Конфигурация SQL компьютера, в какую группу будет добавлена группа</span><span class="sxs-lookup"><span data-stu-id="abcfa-120">The SQL virtual machine configuration which group membership will be added to</span></span>

```yaml
Type: Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMModel
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="abcfa-121">-SqlVMGroup</span><span class="sxs-lookup"><span data-stu-id="abcfa-121">-SqlVMGroup</span></span>
<span data-ttu-id="abcfa-122">Группа, в SQL будет частью виртуальной машины</span><span class="sxs-lookup"><span data-stu-id="abcfa-122">The group the SQL virtual machine will be part of</span></span>

```yaml
Type: Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMGroupModel
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="abcfa-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="abcfa-123">CommonParameters</span></span>
<span data-ttu-id="abcfa-124">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="abcfa-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="abcfa-125">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="abcfa-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="abcfa-126">INPUTS</span><span class="sxs-lookup"><span data-stu-id="abcfa-126">INPUTS</span></span>

### <span data-ttu-id="abcfa-127">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMavire.Model.AzureSqlVMModel</span><span class="sxs-lookup"><span data-stu-id="abcfa-127">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMModel</span></span>

## <span data-ttu-id="abcfa-128">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="abcfa-128">OUTPUTS</span></span>

### <span data-ttu-id="abcfa-129">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMavire.Model.AzureSqlVMModel</span><span class="sxs-lookup"><span data-stu-id="abcfa-129">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMModel</span></span>

## <span data-ttu-id="abcfa-130">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="abcfa-130">NOTES</span></span>

## <span data-ttu-id="abcfa-131">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="abcfa-131">RELATED LINKS</span></span>
