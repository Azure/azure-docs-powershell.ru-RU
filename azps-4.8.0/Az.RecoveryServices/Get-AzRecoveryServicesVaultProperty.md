---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: C2A7F37B-5713-4430-B83F-C6745692396D
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesvaultproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesVaultProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesVaultProperty.md
ms.openlocfilehash: 6602f1005877d4e38546338fd44d8fc51991a7b6
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94234797"
---
# <span data-ttu-id="d3907-101">Get-AzRecoveryServicesVaultProperty</span><span class="sxs-lookup"><span data-stu-id="d3907-101">Get-AzRecoveryServicesVaultProperty</span></span>

## <span data-ttu-id="d3907-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="d3907-102">SYNOPSIS</span></span>
<span data-ttu-id="d3907-103">Возвращает свойства хранилища служб восстановления.</span><span class="sxs-lookup"><span data-stu-id="d3907-103">Returns the properties of a Recovery Services Vault.</span></span>

## <span data-ttu-id="d3907-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="d3907-104">SYNTAX</span></span>

```
Get-AzRecoveryServicesVaultProperty [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="d3907-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d3907-105">DESCRIPTION</span></span>
<span data-ttu-id="d3907-106">Командлет **Get-AzRecoveryServicesVaultProperty** Возвращает свойства хранилища служб восстановления.</span><span class="sxs-lookup"><span data-stu-id="d3907-106">The **Get-AzRecoveryServicesVaultProperty** cmdlet returns the properties of a Recovery services vault.</span></span>

## <span data-ttu-id="d3907-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="d3907-107">EXAMPLES</span></span>

### <span data-ttu-id="d3907-108">Пример 1: получение свойств хранилища</span><span class="sxs-lookup"><span data-stu-id="d3907-108">Example 1: Get Properties of a vault</span></span>
```
PS C:\> $vault = Get-AzRecoveryServicesVault -Name "MyVaultName"
PS C:\> $props = Get-AzRecoveryServicesVaultProperty -VaultId $vault.Id
```

<span data-ttu-id="d3907-109">Первая команда получает объект хранилища и сохраняет его в переменной $vault.</span><span class="sxs-lookup"><span data-stu-id="d3907-109">The first command gets a Vault object and then stores it in the $vault variable.</span></span>
<span data-ttu-id="d3907-110">Вторая команда получает свойства хранилища.</span><span class="sxs-lookup"><span data-stu-id="d3907-110">The second command Gets the Vault Properties.</span></span>

## <span data-ttu-id="d3907-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="d3907-111">PARAMETERS</span></span>

### <span data-ttu-id="d3907-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d3907-112">-DefaultProfile</span></span>
<span data-ttu-id="d3907-113">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="d3907-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d3907-114">-VaultId</span><span class="sxs-lookup"><span data-stu-id="d3907-114">-VaultId</span></span>
<span data-ttu-id="d3907-115">Идентификатор ARM хранилища служб восстановления.</span><span class="sxs-lookup"><span data-stu-id="d3907-115">ARM ID of the Recovery Services Vault.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d3907-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d3907-116">CommonParameters</span></span>
<span data-ttu-id="d3907-117">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="d3907-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d3907-118">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d3907-118">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d3907-119">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="d3907-119">INPUTS</span></span>

### <span data-ttu-id="d3907-120">System. String</span><span class="sxs-lookup"><span data-stu-id="d3907-120">System.String</span></span>

## <span data-ttu-id="d3907-121">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="d3907-121">OUTPUTS</span></span>

### <span data-ttu-id="d3907-122">Microsoft. Azure. Management. RecoveryServices. Backup. Models. BackupResourceVaultConfigResource</span><span class="sxs-lookup"><span data-stu-id="d3907-122">Microsoft.Azure.Management.RecoveryServices.Backup.Models.BackupResourceVaultConfigResource</span></span>

## <span data-ttu-id="d3907-123">Пуск</span><span class="sxs-lookup"><span data-stu-id="d3907-123">NOTES</span></span>

## <span data-ttu-id="d3907-124">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d3907-124">RELATED LINKS</span></span>

[<span data-ttu-id="d3907-125">Get-AzRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="d3907-125">Get-AzRecoveryServicesVault</span></span>](./Get-AzRecoveryServicesVault.md)

[<span data-ttu-id="d3907-126">Set-AzRecoveryServicesVaultProperty</span><span class="sxs-lookup"><span data-stu-id="d3907-126">Set-AzRecoveryServicesVaultProperty</span></span>](./Set-AzRecoveryServicesVaultProperty.md)