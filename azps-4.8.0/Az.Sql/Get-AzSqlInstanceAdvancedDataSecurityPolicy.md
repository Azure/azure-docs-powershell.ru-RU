---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlinstanceadvanceddatasecuritypolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceAdvancedDataSecurityPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceAdvancedDataSecurityPolicy.md
ms.openlocfilehash: 8adb699375a1b53f20e6027f35772642c658928b
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94243257"
---
# <span data-ttu-id="d6040-101">Get-AzSqlInstanceAdvancedDataSecurityPolicy</span><span class="sxs-lookup"><span data-stu-id="d6040-101">Get-AzSqlInstanceAdvancedDataSecurityPolicy</span></span>

## <span data-ttu-id="d6040-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="d6040-102">SYNOPSIS</span></span>
<span data-ttu-id="d6040-103">Получает расширенную политику безопасности данных управляемого экземпляра.</span><span class="sxs-lookup"><span data-stu-id="d6040-103">Gets Advanced Data Security policy of a managed instance.</span></span>

## <span data-ttu-id="d6040-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="d6040-104">SYNTAX</span></span>

```
Get-AzSqlInstanceAdvancedDataSecurityPolicy [-InputObject <AzureSqlManagedInstanceModel>]
 -InstanceName <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="d6040-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d6040-105">DESCRIPTION</span></span>
<span data-ttu-id="d6040-106">Командлет **Get-AzSqlInstanceAdvancedDataSecurityPolicy** извлекает политику повышенной безопасности данных управляемого экземпляра.</span><span class="sxs-lookup"><span data-stu-id="d6040-106">The **Get-AzSqlInstanceAdvancedDataSecurityPolicy** cmdlet retrieves the Advanced Data Security policy of a managed instance.</span></span>

## <span data-ttu-id="d6040-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="d6040-107">EXAMPLES</span></span>

### <span data-ttu-id="d6040-108">Пример 1: получение расширенной защиты данных управляемого экземпляра</span><span class="sxs-lookup"><span data-stu-id="d6040-108">Example 1: Gets managed instance Advanced Data Security</span></span>
```powershell
PS C:\>  Get-AzSqlInstanceAdvancedDataSecurityPolicy `
            -ResourceGroupName "ResourceGroup01" `
            -InstanceName "ManagedInstance01" `

ResourceGroupName            : ResourceGroup01
ManagedInstanceName          : ManagedInstance01
IsEnabled                    : True
```

### <span data-ttu-id="d6040-109">Пример 2: получение расширенной защиты данных управляемого экземпляра для ресурса управляемого экземпляра</span><span class="sxs-lookup"><span data-stu-id="d6040-109">Example 2: Gets managed instance Advanced Data Security from managed instance resource</span></span>
```powershell
PS C:\>  Get-AzSqlInstance `
           -ResourceGroupName "ResourceGroup01" `
           -Name "ManagedInstance01" `
           | Get-AzSqlInstanceAdvancedDataSecurityPolicy

ResourceGroupName            : ResourceGroup01
ManagedInstanceName          : ManagedInstance01
IsEnabled                    : True
```

## <span data-ttu-id="d6040-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="d6040-110">PARAMETERS</span></span>

### <span data-ttu-id="d6040-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d6040-111">-DefaultProfile</span></span>
<span data-ttu-id="d6040-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="d6040-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d6040-113">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d6040-113">-InputObject</span></span>
<span data-ttu-id="d6040-114">Объект управляемого экземпляра для использования с расширенной операцией политики безопасности данных</span><span class="sxs-lookup"><span data-stu-id="d6040-114">The managed instance object to use with Advanced Data Security policy operation</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d6040-115">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="d6040-115">-InstanceName</span></span>
<span data-ttu-id="d6040-116">Имя экземпляра управляемой базы данных SQL.</span><span class="sxs-lookup"><span data-stu-id="d6040-116">SQL Database managed instance name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d6040-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d6040-117">-ResourceGroupName</span></span>
<span data-ttu-id="d6040-118">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="d6040-118">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d6040-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d6040-119">CommonParameters</span></span>
<span data-ttu-id="d6040-120">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="d6040-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d6040-121">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d6040-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d6040-122">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="d6040-122">INPUTS</span></span>

### <span data-ttu-id="d6040-123">Microsoft. Azure. Commands. SQL. ManagedInstance. Model. AzureSqlManagedInstanceModel</span><span class="sxs-lookup"><span data-stu-id="d6040-123">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span></span>

### <span data-ttu-id="d6040-124">System. String</span><span class="sxs-lookup"><span data-stu-id="d6040-124">System.String</span></span>

## <span data-ttu-id="d6040-125">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="d6040-125">OUTPUTS</span></span>

### <span data-ttu-id="d6040-126">Microsoft. Azure. Commands. SQL. AdvancedThreatProtection. Model. ManagedInstanceAdvancedDataSecurityPolicyModel</span><span class="sxs-lookup"><span data-stu-id="d6040-126">Microsoft.Azure.Commands.Sql.AdvancedThreatProtection.Model.ManagedInstanceAdvancedDataSecurityPolicyModel</span></span>

## <span data-ttu-id="d6040-127">Пуск</span><span class="sxs-lookup"><span data-stu-id="d6040-127">NOTES</span></span>

## <span data-ttu-id="d6040-128">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d6040-128">RELATED LINKS</span></span>
