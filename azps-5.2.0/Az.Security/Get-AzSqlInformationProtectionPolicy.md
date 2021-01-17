---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Get-AzSqlInformationProtectionPolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSqlInformationProtectionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSqlInformationProtectionPolicy.md
ms.openlocfilehash: 7f84c3b10577eea0d035c2ce84b3aa8a61af4a3d
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98396060"
---
# <span data-ttu-id="667b4-101">Get-AzSqlInformationProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="667b4-101">Get-AzSqlInformationProtectionPolicy</span></span>

## <span data-ttu-id="667b4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="667b4-102">SYNOPSIS</span></span>
<span data-ttu-id="667b4-103">Извлекает эффективную политику SQL защиты информации.</span><span class="sxs-lookup"><span data-stu-id="667b4-103">Retrieves the effective tenant SQL information protection policy.</span></span>

## <span data-ttu-id="667b4-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="667b4-104">SYNTAX</span></span>

```
Get-AzSqlInformationProtectionPolicy [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="667b4-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="667b4-105">DESCRIPTION</span></span>
<span data-ttu-id="667b4-106">Извлекает эффективную политику защиты информации SQL клиента.</span><span class="sxs-lookup"><span data-stu-id="667b4-106">Retrieves the effective tenant SQL information protection policy.</span></span>

## <span data-ttu-id="667b4-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="667b4-107">EXAMPLES</span></span>

### <span data-ttu-id="667b4-108">Пример</span><span class="sxs-lookup"><span data-stu-id="667b4-108">Example</span></span>
```powershell
PS C:\> Get-AzSqlInformationProtectionPolicy
```

## <span data-ttu-id="667b4-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="667b4-109">PARAMETERS</span></span>

### <span data-ttu-id="667b4-110">-AsJob</span><span class="sxs-lookup"><span data-stu-id="667b4-110">-AsJob</span></span>
<span data-ttu-id="667b4-111">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="667b4-111">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="667b4-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="667b4-112">-DefaultProfile</span></span>
<span data-ttu-id="667b4-113">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="667b4-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="667b4-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="667b4-114">CommonParameters</span></span>
<span data-ttu-id="667b4-115">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="667b4-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="667b4-116">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="667b4-116">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="667b4-117">INPUTS</span><span class="sxs-lookup"><span data-stu-id="667b4-117">INPUTS</span></span>

### <span data-ttu-id="667b4-118">System.string</span><span class="sxs-lookup"><span data-stu-id="667b4-118">System.string</span></span>

## <span data-ttu-id="667b4-119">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="667b4-119">OUTPUTS</span></span>

### <span data-ttu-id="667b4-120">Microsoft.Azure.Commands.SecurityCenter.Models.SqlInformationProtectionPolicy.PSSqlInformationProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="667b4-120">Microsoft.Azure.Commands.SecurityCenter.Models.SqlInformationProtectionPolicy.PSSqlInformationProtectionPolicy</span></span>

## <span data-ttu-id="667b4-121">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="667b4-121">NOTES</span></span>

## <span data-ttu-id="667b4-122">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="667b4-122">RELATED LINKS</span></span>
