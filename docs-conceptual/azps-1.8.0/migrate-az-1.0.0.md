---
title: Все отличия между AzureRM и Az версии 1.0.0 для Azure PowerShell
description: Это руководство по миграции содержит список критических изменений, внесенных в выпуск Az версии 1 в Azure PowerShell.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 05/15/2019
ms.openlocfilehash: ea7593cf2b753b210ff2955b7bd450030ad83596
ms.sourcegitcommit: d661f38bec34e65bf73913db59028e11fd78b131
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/05/2020
ms.locfileid: "75035835"
---
# <a name="breaking-changes-for-az-100"></a><span data-ttu-id="566ce-103">Критические изменения для Az 1.0.0</span><span class="sxs-lookup"><span data-stu-id="566ce-103">Breaking changes for Az 1.0.0</span></span>

<span data-ttu-id="566ce-104">В этом документе содержатся подробные сведения об отличиях между AzureRM 6.x и новым модулем Az версии 1.x и более поздних.</span><span class="sxs-lookup"><span data-stu-id="566ce-104">This document provides detailed information on the changes between AzureRM 6.x and the new Az module, version 1.x and later.</span></span> <span data-ttu-id="566ce-105">Пункты в оглавлении помогут вам разобраться со всеми этапами переноса, включая изменения модуля, которые могут повлиять на скрипты.</span><span class="sxs-lookup"><span data-stu-id="566ce-105">The table of contents will help guide you through a full migration path, including module-specific changes that may affect your scripts.</span></span>

<span data-ttu-id="566ce-106">Общие советы по началу перехода с Az на AzureRM см. в [этой статье](migrate-from-azurerm-to-az.md).</span><span class="sxs-lookup"><span data-stu-id="566ce-106">For general advice on getting started with a migration from AzureRM to Az, see [Start migration from AzureRM to Az](migrate-from-azurerm-to-az.md).</span></span>

## <a name="table-of-contents"></a><span data-ttu-id="566ce-107">Оглавление</span><span class="sxs-lookup"><span data-stu-id="566ce-107">Table of Contents</span></span>

- [<span data-ttu-id="566ce-108">Общие критически важные изменения</span><span class="sxs-lookup"><span data-stu-id="566ce-108">General breaking changes</span></span>](#general-breaking-changes)
  - [<span data-ttu-id="566ce-109">Изменения префикса существительного командлета</span><span class="sxs-lookup"><span data-stu-id="566ce-109">Cmdlet noun prefix changes</span></span>](#cmdlet-noun-prefix-changes)
  - [<span data-ttu-id="566ce-110">Изменение имени модуля</span><span class="sxs-lookup"><span data-stu-id="566ce-110">Module name changes</span></span>](#module-name-changes)
  - [<span data-ttu-id="566ce-111">Удаленные модули</span><span class="sxs-lookup"><span data-stu-id="566ce-111">Removed modules</span></span>](#removed-modules)
  - [<span data-ttu-id="566ce-112">Windows PowerShell 5.1 и .NET 4.7.2</span><span class="sxs-lookup"><span data-stu-id="566ce-112">Windows PowerShell 5.1 and .NET 4.7.2</span></span>](#windows-powershell-51-and-net-472)
  - [<span data-ttu-id="566ce-113">Временное удаление входа пользователя с помощью PSCredential</span><span class="sxs-lookup"><span data-stu-id="566ce-113">Temporary removal of user login using PSCredential</span></span>](#temporary-removal-of-user-login-using-pscredential)
  - [<span data-ttu-id="566ce-114">Вход с кодом устройства по умолчанию вместо запроса веб-браузера</span><span class="sxs-lookup"><span data-stu-id="566ce-114">Default device code login instead of web browser prompt</span></span>](#default-device-code-login-instead-of-web-browser-prompt)
- [<span data-ttu-id="566ce-115">Критические изменения модуля</span><span class="sxs-lookup"><span data-stu-id="566ce-115">Module breaking changes</span></span>](#module-breaking-changes)
  - [<span data-ttu-id="566ce-116">Az.ApiManagement (ранее AzureRM.ApiManagement)</span><span class="sxs-lookup"><span data-stu-id="566ce-116">Az.ApiManagement (previously AzureRM.ApiManagement)</span></span>](#azapimanagement-previously-azurermapimanagement)
  - [<span data-ttu-id="566ce-117">Az.Billing (ранее AzureRM.Billing, AzureRM.Consitation и AzureRM.UsageAggregates)</span><span class="sxs-lookup"><span data-stu-id="566ce-117">Az.Billing (previously AzureRM.Billing, AzureRM.Consumption, and AzureRM.UsageAggregates)</span></span>](#azbilling-previously-azurermbilling-azurermconsumption-and-azurermusageaggregates)
  - [<span data-ttu-id="566ce-118">Az.CognitiveServices (ранее AzureRM.CognitiveServices)</span><span class="sxs-lookup"><span data-stu-id="566ce-118">Az.CognitiveServices (previously AzureRM.CognitiveServices)</span></span>](#azcognitiveservices-previously-azurermcognitiveservices)
  - [<span data-ttu-id="566ce-119">Az.Compute (ранее AzureRM.Compute)</span><span class="sxs-lookup"><span data-stu-id="566ce-119">Az.Compute (previously AzureRM.Compute)</span></span>](#azcompute-previously-azurermcompute)
  - [<span data-ttu-id="566ce-120">Az.DataFactory (ранее AzureRM.DataFactories и AzureRM.DataFactoryV2)</span><span class="sxs-lookup"><span data-stu-id="566ce-120">Az.DataFactory (previously AzureRM.DataFactories and AzureRM.DataFactoryV2)</span></span>](#azdatafactory-previously-azurermdatafactories-and-azurermdatafactoryv2)
  - [<span data-ttu-id="566ce-121">Az.DataLakeAnalytics (ранее AzureRM.DataLakeAnalytics)</span><span class="sxs-lookup"><span data-stu-id="566ce-121">Az.DataLakeAnalytics (previously AzureRM.DataLakeAnalytics)</span></span>](#azdatalakeanalytics-previously-azurermdatalakeanalytics)
  - [<span data-ttu-id="566ce-122">Az.DataLakeStore (ранее AzureRM.DataLakeStore)</span><span class="sxs-lookup"><span data-stu-id="566ce-122">Az.DataLakeStore (previously AzureRM.DataLakeStore)</span></span>](#azdatalakestore-previously-azurermdatalakestore)
  - [<span data-ttu-id="566ce-123">Az.KeyVault (ранее AzureRM.KeyVault)</span><span class="sxs-lookup"><span data-stu-id="566ce-123">Az.KeyVault (previously AzureRM.KeyVault)</span></span>](#azkeyvault-previously-azurermkeyvault)
  - [<span data-ttu-id="566ce-124">Az.Media (ранее AzureRM.Media)</span><span class="sxs-lookup"><span data-stu-id="566ce-124">Az.Media (previously AzureRM.Media)</span></span>](#azmedia-previously-azurermmedia)
  - [<span data-ttu-id="566ce-125">Az.Monitor (ранее AzureRM.Insights)</span><span class="sxs-lookup"><span data-stu-id="566ce-125">Az.Monitor (previously AzureRM.Insights)</span></span>](#azmonitor-previously-azurerminsights)
  - [<span data-ttu-id="566ce-126">Az.Network (ранее AzureRM.Network)</span><span class="sxs-lookup"><span data-stu-id="566ce-126">Az.Network (previously AzureRM.Network)</span></span>](#aznetwork-previously-azurermnetwork)
  - [<span data-ttu-id="566ce-127">Az.OperationalInsights (ранее AzureRM.OperationalInsights)</span><span class="sxs-lookup"><span data-stu-id="566ce-127">Az.OperationalInsights (previously AzureRM.OperationalInsights)</span></span>](#azoperationalinsights-previously-azurermoperationalinsights)
  - [<span data-ttu-id="566ce-128">Az.RecoveryServices (ранее AzureRM.RecoveryServices, AzureRM.RecoveryServices.Backup и AzureRM.RecoveryServices.SiteRecovery)</span><span class="sxs-lookup"><span data-stu-id="566ce-128">Az.RecoveryServices (previously AzureRM.RecoveryServices, AzureRM.RecoveryServices.Backup, and AzureRM.RecoveryServices.SiteRecovery)</span></span>](#azrecoveryservices-previously-azurermrecoveryservices-azurermrecoveryservicesbackup-and-azurermrecoveryservicessiterecovery)
  - [<span data-ttu-id="566ce-129">Az.Resources (ранее AzureRM.Resources)</span><span class="sxs-lookup"><span data-stu-id="566ce-129">Az.Resources (previously AzureRM.Resources)</span></span>](#azresources-previously-azurermresources)
  - [<span data-ttu-id="566ce-130">Az.ServiceFabric (ранее AzureRM.ServiceFabric)</span><span class="sxs-lookup"><span data-stu-id="566ce-130">Az.ServiceFabric (previously AzureRM.ServiceFabric)</span></span>](#azservicefabric-previously-azurermservicefabric)
  - [<span data-ttu-id="566ce-131">Az.Sql (ранее AzureRM.Sql)</span><span class="sxs-lookup"><span data-stu-id="566ce-131">Az.Sql (previously AzureRM.Sql)</span></span>](#azsql-previously-azurermsql)
  - [<span data-ttu-id="566ce-132">Az.Storage (ранее Azure.Storage и AzureRM.Storage)</span><span class="sxs-lookup"><span data-stu-id="566ce-132">Az.Storage (previously Azure.Storage and AzureRM.Storage)</span></span>](#azstorage-previously-azurestorage-and-azurermstorage)
  - [<span data-ttu-id="566ce-133">Az.Websites (ранее AzureRM.Websites)</span><span class="sxs-lookup"><span data-stu-id="566ce-133">Az.Websites (previously AzureRM.Websites)</span></span>](#azwebsites-previously-azurermwebsites)

## <a name="general-breaking-changes"></a><span data-ttu-id="566ce-134">Общие критически важные изменения</span><span class="sxs-lookup"><span data-stu-id="566ce-134">General breaking changes</span></span>

<span data-ttu-id="566ce-135">В этом разделе описаны общие критические изменения, которые являются частью этой переработанной версии модуля Az.</span><span class="sxs-lookup"><span data-stu-id="566ce-135">This section details the general breaking changes that are part of the redesign of the Az module.</span></span>

### <a name="cmdlet-noun-prefix-changes"></a><span data-ttu-id="566ce-136">Изменения префикса существительного командлета</span><span class="sxs-lookup"><span data-stu-id="566ce-136">Cmdlet Noun Prefix Changes</span></span>

<span data-ttu-id="566ce-137">В модуле AzureRM в существительных командлетов используется префикс `AzureRM` или `Azure`.</span><span class="sxs-lookup"><span data-stu-id="566ce-137">In the AzureRM module, cmdlets used either `AzureRM` or `Azure` as a noun prefix.</span></span>  <span data-ttu-id="566ce-138">Az упрощает и нормализует имена командлетов, так что все командлеты используют "Az" в качестве префикса существительного командлета.</span><span class="sxs-lookup"><span data-stu-id="566ce-138">Az simplifies and normalizes cmdlet names, so that all cmdlets use 'Az' as their cmdlet noun prefix.</span></span> <span data-ttu-id="566ce-139">Пример:</span><span class="sxs-lookup"><span data-stu-id="566ce-139">For example:</span></span>

```azurepowershell-interactive
Get-AzureRMVM
Get-AzureKeyVaultSecret
```

<span data-ttu-id="566ce-140">изменено на:</span><span class="sxs-lookup"><span data-stu-id="566ce-140">Has changed to:</span></span>

```azurepowershell-interactive
Get-AzVM
Get-AzKeyVaultSecret
```

<span data-ttu-id="566ce-141">Чтобы упростить переход на эти новые имена командлетов, Az представляет два новых командлета: [Enable-AzureRmAlias](/powershell/module/az.accounts/enable-azurermalias) и [Disable-AzureRmAlias](/powershell/module/az.accounts/disable-azurermalias).</span><span class="sxs-lookup"><span data-stu-id="566ce-141">To make the transition to these new cmdlet names simpler, Az introduces two new cmdlets, [Enable-AzureRmAlias](/powershell/module/az.accounts/enable-azurermalias) and [Disable-AzureRmAlias](/powershell/module/az.accounts/disable-azurermalias).</span></span>  <span data-ttu-id="566ce-142">`Enable-AzureRmAlias` создает псевдонимы для старых имен командлетов в AzureRM, которые сопоставляются с новыми именами командлетов Az.</span><span class="sxs-lookup"><span data-stu-id="566ce-142">`Enable-AzureRmAlias` creates aliases for the older cmdlet names in AzureRM that map to the newer Az cmdlet names.</span></span> <span data-ttu-id="566ce-143">Используя аргумент `-Scope` с командлетом `Enable-AzureRmAlias`, вы можете выбрать, в контексте чего будут включены псевдонимы.</span><span class="sxs-lookup"><span data-stu-id="566ce-143">Using the `-Scope` argument with `Enable-AzureRmAlias` allows you to choose where aliases are enabled.</span></span>

<span data-ttu-id="566ce-144">Следующий сценарий в AzureRM является примером.</span><span class="sxs-lookup"><span data-stu-id="566ce-144">For example, the following script in AzureRM:</span></span>

```azurepowershell-interactive
#Requires -Modules AzureRM.Storage
Get-AzureRmStorageAccount | Get-AzureStorageContainer | Get-AzureStorageBlob
```

<span data-ttu-id="566ce-145">Его можно выполнить с минимальными изменениями с помощью `Enable-AzureRmAlias`.</span><span class="sxs-lookup"><span data-stu-id="566ce-145">Can be run with minimal changes using `Enable-AzureRmAlias`:</span></span>

```azurepowershell-interactive
#Requires -Modules Az.Storage
Enable-AzureRmAlias -Scope Process
Get-AzureRmStorageAccount | Get-AzureStorageContainer | Get-AzureStorageBlob
```

<span data-ttu-id="566ce-146">При выполнении `Enable-AzureRmAlias -Scope CurrentUser` псевдонимы будут включены для всех открытых сеансов PowerShell, так что после выполнения этого командлета такой сценарий не нужно будет изменять.</span><span class="sxs-lookup"><span data-stu-id="566ce-146">Running `Enable-AzureRmAlias -Scope CurrentUser` will enable the aliases for all PowerShell sessions you open, so that after executing this cmdlet, a script like this would not need to be changed at all:</span></span>

```azurepowershell-interactive
Get-AzureRmStorageAccount | Get-AzureStorageContainer | Get-AzureStorageBlob
```

<span data-ttu-id="566ce-147">Дополнительные сведения об использовании командлетов псевдонимов см. в [справочнике по командлету Enable-AzureRmAlias](/powershell/module/az.accounts/enable-azurermalias).</span><span class="sxs-lookup"><span data-stu-id="566ce-147">For complete details on the usage of the alias cmdlets, see the [Enable-AzureRmAlias reference](/powershell/module/az.accounts/enable-azurermalias).</span></span>

<span data-ttu-id="566ce-148">Когда вы будете готовы отключить псевдонимы, запустите командлет `Disable-AzureRmAlias`, который удаляет созданные псевдонимы.</span><span class="sxs-lookup"><span data-stu-id="566ce-148">When you're ready to disable aliases, `Disable-AzureRmAlias` removes the created aliases.</span></span> <span data-ttu-id="566ce-149">Дополнительные сведения см. в [справочнике по командлету Disable-AzureRmAlias](/powershell/module/az.accounts/disable-azurermalias).</span><span class="sxs-lookup"><span data-stu-id="566ce-149">For complete details, see the [Disable-AzureRmAlias reference](/powershell/module/az.accounts/disable-azurermalias).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="566ce-150">Убедитесь, что отключили псевдонимы для _всех_ областей, в которых они были включены.</span><span class="sxs-lookup"><span data-stu-id="566ce-150">When disabling aliases, make sure that they are disabled for _all_ scopes which had aliases enabled.</span></span>

### <a name="module-name-changes"></a><span data-ttu-id="566ce-151">Изменение имени модуля</span><span class="sxs-lookup"><span data-stu-id="566ce-151">Module Name Changes</span></span>

<span data-ttu-id="566ce-152">Имена модулей изменены с `AzureRM.*` на `Az.*`, за исключением следующих модулей.</span><span class="sxs-lookup"><span data-stu-id="566ce-152">The module names have changed from `AzureRM.*` to `Az.*`, except for the following modules:</span></span>

| <span data-ttu-id="566ce-153">Модуль AzureRM</span><span class="sxs-lookup"><span data-stu-id="566ce-153">AzureRM module</span></span> | <span data-ttu-id="566ce-154">Модуль Az</span><span class="sxs-lookup"><span data-stu-id="566ce-154">Az module</span></span> |
|----------------|-----------|
| <span data-ttu-id="566ce-155">Azure.Storage;</span><span class="sxs-lookup"><span data-stu-id="566ce-155">Azure.Storage</span></span> | <span data-ttu-id="566ce-156">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="566ce-156">Az.Storage</span></span> |
| <span data-ttu-id="566ce-157">Azure.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="566ce-157">Azure.AnalysisServices</span></span> | <span data-ttu-id="566ce-158">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="566ce-158">Az.AnalysisServices</span></span> |
| <span data-ttu-id="566ce-159">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="566ce-159">AzureRM.Profile</span></span> | <span data-ttu-id="566ce-160">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="566ce-160">Az.Accounts</span></span> |
| <span data-ttu-id="566ce-161">AzureRM.Insights;</span><span class="sxs-lookup"><span data-stu-id="566ce-161">AzureRM.Insights</span></span> | <span data-ttu-id="566ce-162">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="566ce-162">Az.Monitor</span></span> |
| <span data-ttu-id="566ce-163">AzureRM.DataFactories</span><span class="sxs-lookup"><span data-stu-id="566ce-163">AzureRM.DataFactories</span></span> | <span data-ttu-id="566ce-164">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="566ce-164">Az.DataFactory</span></span> |
| <span data-ttu-id="566ce-165">AzureRM.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="566ce-165">AzureRM.DataFactoryV2</span></span> | <span data-ttu-id="566ce-166">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="566ce-166">Az.DataFactory</span></span> |
| <span data-ttu-id="566ce-167">AzureRM.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="566ce-167">AzureRM.RecoveryServices.Backup</span></span> | <span data-ttu-id="566ce-168">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="566ce-168">Az.RecoveryServices</span></span> |
| <span data-ttu-id="566ce-169">AzureRM.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="566ce-169">AzureRM.RecoveryServices.SiteRecovery</span></span> | <span data-ttu-id="566ce-170">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="566ce-170">Az.RecoveryServices</span></span> |
| <span data-ttu-id="566ce-171">AzureRM.Tags</span><span class="sxs-lookup"><span data-stu-id="566ce-171">AzureRM.Tags</span></span> | <span data-ttu-id="566ce-172">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="566ce-172">Az.Resources</span></span> |
| <span data-ttu-id="566ce-173">AzureRM.MachineLearningCompute</span><span class="sxs-lookup"><span data-stu-id="566ce-173">AzureRM.MachineLearningCompute</span></span> | <span data-ttu-id="566ce-174">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="566ce-174">Az.MachineLearning</span></span> |
| <span data-ttu-id="566ce-175">AzureRM.UsageAggregates</span><span class="sxs-lookup"><span data-stu-id="566ce-175">AzureRM.UsageAggregates</span></span> | <span data-ttu-id="566ce-176">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="566ce-176">Az.Billing</span></span> |
| <span data-ttu-id="566ce-177">AzureRM.Consumption:</span><span class="sxs-lookup"><span data-stu-id="566ce-177">AzureRM.Consumption</span></span> | <span data-ttu-id="566ce-178">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="566ce-178">Az.Billing</span></span> |

<span data-ttu-id="566ce-179">Изменения в именах модулей означают, что любой сценарий, который использует `#Requires` или `Import-Module` для загрузки определенных модулей, необходимо будет изменить, чтобы вместо него использовать новый модуль.</span><span class="sxs-lookup"><span data-stu-id="566ce-179">The changes in module names mean that any script that uses `#Requires` or `Import-Module` to load specific modules will need to be changed to use the new module instead.</span></span> <span data-ttu-id="566ce-180">Для модулей, в которых суффикс командлета не был изменен, это означает, что хотя имя модуля изменилось, суффикс, указывающий пространство операции, _не изменился_.</span><span class="sxs-lookup"><span data-stu-id="566ce-180">For modules where the cmdlet suffix has not changed, this means that although the module name has changed, the suffix indicating the operation space has _not_.</span></span>

#### <a name="migrating-requires-and-import-module-statements"></a><span data-ttu-id="566ce-181">Перенос инструкций #Requires и Import-Module</span><span class="sxs-lookup"><span data-stu-id="566ce-181">Migrating #Requires and Import-Module Statements</span></span>

<span data-ttu-id="566ce-182">Скрипты, объявляющие зависимости от модулей AzureRM с помощью `#Requires` или `Import-Module`, должны быть обновлены для использования новых имен модулей.</span><span class="sxs-lookup"><span data-stu-id="566ce-182">Scripts that use `#Requires` or `Import-Module` to declare a dependency on AzureRM modules must be updated to use the new module names.</span></span> <span data-ttu-id="566ce-183">Пример:</span><span class="sxs-lookup"><span data-stu-id="566ce-183">For example:</span></span>

```azurepowershell-interactive
#Requires -Module AzureRM.Compute
```

<span data-ttu-id="566ce-184">следует изменить на</span><span class="sxs-lookup"><span data-stu-id="566ce-184">Should be changed to:</span></span>

```azurepowershell-interactive
#Requires -Module Az.Compute
```

<span data-ttu-id="566ce-185">Для `Import-Module`:</span><span class="sxs-lookup"><span data-stu-id="566ce-185">For `Import-Module`:</span></span>

```azurepowershell-interactive
Import-Module -Name AzureRM.Compute
```

<span data-ttu-id="566ce-186">следует изменить на</span><span class="sxs-lookup"><span data-stu-id="566ce-186">Should be changed to:</span></span>

```azurepowershell-interactive
Import-Module -Name Az.Compute
```

### <a name="migrating-fully-qualified-cmdlet-invocations"></a><span data-ttu-id="566ce-187">Миграция вызовов командлета Fully-Qualified</span><span class="sxs-lookup"><span data-stu-id="566ce-187">Migrating Fully-Qualified Cmdlet Invocations</span></span>

<span data-ttu-id="566ce-188">Скрипты, использующие вызовы командлетов с указанием модуля, например:</span><span class="sxs-lookup"><span data-stu-id="566ce-188">Scripts that use module-qualified cmdlet invocations, such as:</span></span>

```azurepowershell-interactive
AzureRM.Compute\Get-AzureRmVM
```

<span data-ttu-id="566ce-189">Следует изменить, чтобы использовать новые имена модулей и командлетов:</span><span class="sxs-lookup"><span data-stu-id="566ce-189">Must be changed to use the new module and cmdlet names:</span></span>

```azurepowershell-interactive
Az.Compute\Get-AzVM
```

### <a name="migrating-module-manifest-dependencies"></a><span data-ttu-id="566ce-190">Перенос зависимостей манифеста модуля</span><span class="sxs-lookup"><span data-stu-id="566ce-190">Migrating module manifest dependencies</span></span>

<span data-ttu-id="566ce-191">Модули, которые выражают зависимости от модулей AzureRM через файл манифеста модуля (PSD1), должны обновить имена модулей в разделе `RequiredModules`.</span><span class="sxs-lookup"><span data-stu-id="566ce-191">Modules that express dependencies on AzureRM modules through a module manifest (.psd1) file will need to updated the module names in their `RequiredModules` section:</span></span>

```powershell
RequiredModules = @(@{ModuleName="AzureRM.Profile"; ModuleVersion="5.8.2"})
```

<span data-ttu-id="566ce-192">Необходимо изменить на:</span><span class="sxs-lookup"><span data-stu-id="566ce-192">Must be changed to:</span></span>

```powershell
RequiredModules = @(@{ModuleName="Az.Profile"; ModuleVersion="1.0.0"})
```

### <a name="removed-modules"></a><span data-ttu-id="566ce-193">Удаленные модули</span><span class="sxs-lookup"><span data-stu-id="566ce-193">Removed modules</span></span>

<span data-ttu-id="566ce-194">Следующие модули удалены:</span><span class="sxs-lookup"><span data-stu-id="566ce-194">The following modules have been removed:</span></span>

- `AzureRM.Backup`
- `AzureRM.Compute.ManagedService`
- `AzureRM.Scheduler`

<span data-ttu-id="566ce-195">Средства для работы с этими службами больше не поддерживаются.</span><span class="sxs-lookup"><span data-stu-id="566ce-195">The tools for these services are no longer actively supported.</span></span>  <span data-ttu-id="566ce-196">Клиентам рекомендуется обратиться к альтернативным службам, как только появится возможность.</span><span class="sxs-lookup"><span data-stu-id="566ce-196">Customers are encouraged to move to alternative services as soon as it is convenient.</span></span>

### <a name="windows-powershell-51-and-net-472"></a><span data-ttu-id="566ce-197">Windows PowerShell 5.1 и .NET 4.7.2</span><span class="sxs-lookup"><span data-stu-id="566ce-197">Windows PowerShell 5.1 and .NET 4.7.2</span></span>

<span data-ttu-id="566ce-198">Для использования Az с PowerShell 5.1 для Windows требуется установить .NET Framework 4.7.2.</span><span class="sxs-lookup"><span data-stu-id="566ce-198">Using Az with PowerShell 5.1 for Windows requires the installation of .NET Framework 4.7.2.</span></span> <span data-ttu-id="566ce-199">Для использования PowerShell Core 6.x или более поздней версии .NET Framework не требуется.</span><span class="sxs-lookup"><span data-stu-id="566ce-199">Using PowerShell Core 6.x or later does not require .NET Framework.</span></span>

### <a name="temporary-removal-of-user-login-using-pscredential"></a><span data-ttu-id="566ce-200">Временное удаление входа пользователя с помощью PSCredential</span><span class="sxs-lookup"><span data-stu-id="566ce-200">Temporary removal of User login using PSCredential</span></span>

<span data-ttu-id="566ce-201">Из-за изменений в процессе проверки подлинности для .NET Standard мы временно удаляем вход пользователя через PSCredential.</span><span class="sxs-lookup"><span data-stu-id="566ce-201">Due to changes in the authentication flow for .NET Standard, we are temporarily removing user login via PSCredential.</span></span> <span data-ttu-id="566ce-202">Эта возможность будет доступна в выпуске от 15 января 2019 г. для Windows PowerShell 5.1.</span><span class="sxs-lookup"><span data-stu-id="566ce-202">This capability will be re-introduced in the 1/15/2019 release for PowerShell 5.1 for Windows.</span></span> <span data-ttu-id="566ce-203">Это подробно описано в [этом сообщении на сайте GitHub](https://github.com/Azure/azure-powershell/issues/7430).</span><span class="sxs-lookup"><span data-stu-id="566ce-203">This is discussed in detail in [this GitHub issue.](https://github.com/Azure/azure-powershell/issues/7430)</span></span>

### <a name="default-device-code-login-instead-of-web-browser-prompt"></a><span data-ttu-id="566ce-204">Вход с кодом устройства по умолчанию вместо запроса веб-браузера</span><span class="sxs-lookup"><span data-stu-id="566ce-204">Default device code login instead of web browser prompt</span></span>

<span data-ttu-id="566ce-205">Из-за изменений в процессе проверки подлинности для .NET Standard мы используем вход устройства в качестве потока входа по умолчанию во время интерактивного входа.</span><span class="sxs-lookup"><span data-stu-id="566ce-205">Due to changes in the authentication flow for .NET Standard, we are using device login as the default login flow during interactive login.</span></span> <span data-ttu-id="566ce-206">Вход через веб-браузер будет повторно представлен для Windows PowerShell 5.1 в качестве версии по умолчанию в выпуске от 15 января 2019 г.</span><span class="sxs-lookup"><span data-stu-id="566ce-206">Web browser based login will be re-introduced for PowerShell 5.1 for Windows as the default in the 1/15/2019 release.</span></span> <span data-ttu-id="566ce-207">В это время пользователи смогут выбрать вход устройства с помощью параметра Switch.</span><span class="sxs-lookup"><span data-stu-id="566ce-207">At that time, users will be able to choose device login using a Switch parameter.</span></span>

## <a name="module-breaking-changes"></a><span data-ttu-id="566ce-208">Критические изменения модуля</span><span class="sxs-lookup"><span data-stu-id="566ce-208">Module breaking changes</span></span>

<span data-ttu-id="566ce-209">В этом разделе описаны конкретные критические изменения для отдельных модулей и командлетов.</span><span class="sxs-lookup"><span data-stu-id="566ce-209">This section details specific breaking changes for individual modules and cmdlets.</span></span>

### <a name="azapimanagement-previously-azurermapimanagement"></a><span data-ttu-id="566ce-210">Az.ApiManagement (ранее AzureRM.ApiManagement)</span><span class="sxs-lookup"><span data-stu-id="566ce-210">Az.ApiManagement (previously AzureRM.ApiManagement)</span></span>

- <span data-ttu-id="566ce-211">Удалены приведенные ниже командлеты.</span><span class="sxs-lookup"><span data-stu-id="566ce-211">Removed the following cmdlets:</span></span>
  - <span data-ttu-id="566ce-212">New-AzureRmApiManagementHostnameConfiguration</span><span class="sxs-lookup"><span data-stu-id="566ce-212">New-AzureRmApiManagementHostnameConfiguration</span></span>
  - <span data-ttu-id="566ce-213">Set-AzureRmApiManagementHostnames</span><span class="sxs-lookup"><span data-stu-id="566ce-213">Set-AzureRmApiManagementHostnames</span></span>
  - <span data-ttu-id="566ce-214">Update-AzureRmApiManagementDeployment</span><span class="sxs-lookup"><span data-stu-id="566ce-214">Update-AzureRmApiManagementDeployment</span></span>
  - <span data-ttu-id="566ce-215">Import-AzureRmApiManagementHostnameCertificate</span><span class="sxs-lookup"><span data-stu-id="566ce-215">Import-AzureRmApiManagementHostnameCertificate</span></span>
  - <span data-ttu-id="566ce-216">Используйте командлет **Set-AzApiManagement**, чтобы задать эти свойства.</span><span class="sxs-lookup"><span data-stu-id="566ce-216">Use **Set-AzApiManagement** cmdlet to set these properties instead</span></span>
- <span data-ttu-id="566ce-217">Удалены приведенные ниже свойства.</span><span class="sxs-lookup"><span data-stu-id="566ce-217">Removed the following properties:</span></span>
  - <span data-ttu-id="566ce-218">Удалены свойства: `PortalHostnameConfiguration`, `ProxyHostnameConfiguration`, `ManagementHostnameConfiguration` и `ScmHostnameConfiguration` типа `PsApiManagementHostnameConfiguration` из `PsApiManagementContext`.</span><span class="sxs-lookup"><span data-stu-id="566ce-218">Removed property `PortalHostnameConfiguration`, `ProxyHostnameConfiguration`, `ManagementHostnameConfiguration` and `ScmHostnameConfiguration` of type `PsApiManagementHostnameConfiguration` from `PsApiManagementContext`.</span></span> <span data-ttu-id="566ce-219">Вместо этого используйте: `PortalCustomHostnameConfiguration`, `ProxyCustomHostnameConfiguration`, `ManagementCustomHostnameConfiguration` и `ScmCustomHostnameConfiguration` типа `PsApiManagementCustomHostNameConfiguration`.</span><span class="sxs-lookup"><span data-stu-id="566ce-219">Instead use `PortalCustomHostnameConfiguration`, `ProxyCustomHostnameConfiguration`, `ManagementCustomHostnameConfiguration` and `ScmCustomHostnameConfiguration` of type `PsApiManagementCustomHostNameConfiguration`.</span></span>
  - <span data-ttu-id="566ce-220">Свойство `StaticIPs` удалено из PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="566ce-220">Removed property `StaticIPs` from PsApiManagementContext.</span></span> <span data-ttu-id="566ce-221">Свойство было разделено на `PublicIPAddresses` и `PrivateIPAddresses`.</span><span class="sxs-lookup"><span data-stu-id="566ce-221">The property has been split into `PublicIPAddresses` and `PrivateIPAddresses`.</span></span>
  - <span data-ttu-id="566ce-222">Обязательное свойство `Location` удалено из командлета New-AzureApiManagementVirtualNetwork.</span><span class="sxs-lookup"><span data-stu-id="566ce-222">Removed required property `Location` from New-AzureApiManagementVirtualNetwork cmdlet.</span></span>

### <a name="azbilling-previously-azurermbilling-azurermconsumption-and-azurermusageaggregates"></a><span data-ttu-id="566ce-223">Az.Billing (ранее AzureRM.Billing, AzureRM.Consitation и AzureRM.UsageAggregates)</span><span class="sxs-lookup"><span data-stu-id="566ce-223">Az.Billing (previously AzureRM.Billing, AzureRM.Consumption, and AzureRM.UsageAggregates)</span></span>

- <span data-ttu-id="566ce-224">Параметр `InvoiceName` удален из командлета `Get-AzConsumptionUsageDetail`.</span><span class="sxs-lookup"><span data-stu-id="566ce-224">The `InvoiceName` parameter was removed from the `Get-AzConsumptionUsageDetail` cmdlet.</span></span>  <span data-ttu-id="566ce-225">Для сценариев необходимо использовать другие параметры идентификации для счета.</span><span class="sxs-lookup"><span data-stu-id="566ce-225">Scripts will need to use other identity parameters for the invoice.</span></span>

### <a name="azcognitiveservices-previously-azurermcognitiveservices"></a><span data-ttu-id="566ce-226">Az.CognitiveServices (ранее AzureRM.CognitiveServices)</span><span class="sxs-lookup"><span data-stu-id="566ce-226">Az.CognitiveServices (previously AzureRM.CognitiveServices)</span></span>

- <span data-ttu-id="566ce-227">Набор параметров `GetSkusWithAccountParamSetName` удален из командлета `Get-AzCognitiveServicesAccountSkus`.</span><span class="sxs-lookup"><span data-stu-id="566ce-227">Removed `GetSkusWithAccountParamSetName` parameter set from `Get-AzCognitiveServicesAccountSkus` cmdlet.</span></span>  <span data-ttu-id="566ce-228">Необходимо получить Skus по типу и расположению учетной записи, а не использовать ResourceGroupName и имя учетной записи.</span><span class="sxs-lookup"><span data-stu-id="566ce-228">You must get Skus by Account Type and Location, instead of using ResourceGroupName and Account Name.</span></span>

### <a name="azcompute-previously-azurermcompute"></a><span data-ttu-id="566ce-229">Az.Compute (ранее AzureRM.Compute)</span><span class="sxs-lookup"><span data-stu-id="566ce-229">Az.Compute (previously AzureRM.Compute)</span></span>

- <span data-ttu-id="566ce-230">`IdentityIds` удалены из свойства `Identity` в объектах `PSVirtualMachine` и `PSVirtualMachineScaleSet`. Сценарии больше не должны использовать значение этого поля для принятия решений об обработке.</span><span class="sxs-lookup"><span data-stu-id="566ce-230">`IdentityIds` are removed from `Identity` property in `PSVirtualMachine` and `PSVirtualMachineScaleSet` objects Scripts should no longer use the value of this field to make processing decisions.</span></span>
- <span data-ttu-id="566ce-231">Тип свойства `InstanceView` объекта `PSVirtualMachineScaleSetVM` изменен с `VirtualMachineInstanceView` на `VirtualMachineScaleSetVMInstanceView`</span><span class="sxs-lookup"><span data-stu-id="566ce-231">The type of `InstanceView` property of `PSVirtualMachineScaleSetVM` object is changed from `VirtualMachineInstanceView` to `VirtualMachineScaleSetVMInstanceView`</span></span>
- <span data-ttu-id="566ce-232">Свойства `AutoOSUpgradePolicy` и `AutomaticOSUpgrade` удалены из свойства `UpgradePolicy`</span><span class="sxs-lookup"><span data-stu-id="566ce-232">`AutoOSUpgradePolicy` and `AutomaticOSUpgrade` properties are removed from `UpgradePolicy` property</span></span>
- <span data-ttu-id="566ce-233">Тип свойства `Sku` в объекте `PSSnapshotUpdate` изменен с `DiskSku` на `SnapshotSku`</span><span class="sxs-lookup"><span data-stu-id="566ce-233">The type of `Sku` property in `PSSnapshotUpdate` object is changed from `DiskSku` to `SnapshotSku`</span></span>
- <span data-ttu-id="566ce-234">Параметр `VmScaleSetVMParameterSet` удален из командлета `Add-AzVMDataDisk`. Больше нельзя отдельно добавлять диск данных в виртуальную машину из масштабируемого набора.</span><span class="sxs-lookup"><span data-stu-id="566ce-234">`VmScaleSetVMParameterSet` is removed from `Add-AzVMDataDisk` cmdlet, you can no longer add a data disk individually to a ScaleSet VM.</span></span>

### <a name="azdatafactory-previously-azurermdatafactories-and-azurermdatafactoryv2"></a><span data-ttu-id="566ce-235">Az.DataFactory (ранее AzureRM.DataFactories и AzureRM.DataFactoryV2)</span><span class="sxs-lookup"><span data-stu-id="566ce-235">Az.DataFactory (previously AzureRM.DataFactories and AzureRM.DataFactoryV2)</span></span>

- <span data-ttu-id="566ce-236">Параметр `GatewayName` стал обязательным в командлете `New-AzDataFactoryEncryptValue`</span><span class="sxs-lookup"><span data-stu-id="566ce-236">The `GatewayName` parameter has become mandatory in the `New-AzDataFactoryEncryptValue` cmdlet</span></span>
- <span data-ttu-id="566ce-237">Командлет `New-AzDataFactoryGatewayKey` удалено</span><span class="sxs-lookup"><span data-stu-id="566ce-237">Removed `New-AzDataFactoryGatewayKey` cmdlet</span></span>
- <span data-ttu-id="566ce-238">Параметр `LinkedServiceName` удален из командлета `Get-AzDataFactoryV2ActivityRun`. Сценарии больше не должны использовать значение этого поля для принятия решений об обработке.</span><span class="sxs-lookup"><span data-stu-id="566ce-238">Removed `LinkedServiceName` parameter from `Get-AzDataFactoryV2ActivityRun` cmdlet Scripts should no longer use the value of this field to make processing decisions.</span></span>

### <a name="azdatalakeanalytics-previously-azurermdatalakeanalytics"></a><span data-ttu-id="566ce-239">Az.DataLakeAnalytics (ранее AzureRM.DataLakeAnalytics)</span><span class="sxs-lookup"><span data-stu-id="566ce-239">Az.DataLakeAnalytics (previously AzureRM.DataLakeAnalytics)</span></span>

- <span data-ttu-id="566ce-240">Удалены следующие нерекомендуемые командлеты: `New-AzDataLakeAnalyticsCatalogSecret`, `Remove-AzDataLakeAnalyticsCatalogSecret` и `Set-AzDataLakeAnalyticsCatalogSecret`.</span><span class="sxs-lookup"><span data-stu-id="566ce-240">Removed deprecated cmdlets: `New-AzDataLakeAnalyticsCatalogSecret`, `Remove-AzDataLakeAnalyticsCatalogSecret`, and `Set-AzDataLakeAnalyticsCatalogSecret`</span></span>

### <a name="azdatalakestore-previously-azurermdatalakestore"></a><span data-ttu-id="566ce-241">Az.DataLakeStore (ранее AzureRM.DataLakeStore)</span><span class="sxs-lookup"><span data-stu-id="566ce-241">Az.DataLakeStore (previously AzureRM.DataLakeStore)</span></span>

- <span data-ttu-id="566ce-242">В следующих командлетах параметр `Encoding` изменен с типа `FileSystemCmdletProviderEncoding` на `System.Text.Encoding`.</span><span class="sxs-lookup"><span data-stu-id="566ce-242">The following cmdlets have had the `Encoding` parameter changed from the type `FileSystemCmdletProviderEncoding` to `System.Text.Encoding`.</span></span> <span data-ttu-id="566ce-243">Это изменение удаляет значения кодирования `String` и `Oem`.</span><span class="sxs-lookup"><span data-stu-id="566ce-243">This change removes the encoding values `String` and `Oem`.</span></span> <span data-ttu-id="566ce-244">Все остальные предыдущие значения кодирования остаются.</span><span class="sxs-lookup"><span data-stu-id="566ce-244">All the other prior encoding values remain.</span></span>
  - <span data-ttu-id="566ce-245">New-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="566ce-245">New-AzureRmDataLakeStoreItem</span></span>
  - <span data-ttu-id="566ce-246">Add-AzureRmDataLakeStoreItemContent</span><span class="sxs-lookup"><span data-stu-id="566ce-246">Add-AzureRmDataLakeStoreItemContent</span></span>
  - <span data-ttu-id="566ce-247">Get-AzureRmDataLakeStoreItemContent</span><span class="sxs-lookup"><span data-stu-id="566ce-247">Get-AzureRmDataLakeStoreItemContent</span></span>
- <span data-ttu-id="566ce-248">Удален нерекомендуемый псевдоним свойства `Tags` из командлетов `New-AzDataLakeStoreAccount` и `Set-AzDataLakeStoreAccount`.</span><span class="sxs-lookup"><span data-stu-id="566ce-248">Removed deprecated `Tags` property alias from `New-AzDataLakeStoreAccount` and `Set-AzDataLakeStoreAccount` cmdlets</span></span>

  <span data-ttu-id="566ce-249">Сценарии, которые используют</span><span class="sxs-lookup"><span data-stu-id="566ce-249">Scripts using</span></span>
  ```azurepowershell-interactive
  New-AzureRMDataLakeStoreAccount -Tags @{TagName="TagValue"}
  ```

  <span data-ttu-id="566ce-250">следует изменить на</span><span class="sxs-lookup"><span data-stu-id="566ce-250">Should be changed to</span></span>
  ```azurepowershell-interactive
  New-AzDataLakeStoreAccount -Tag @{TagName="TagValue"}
  ```

- <span data-ttu-id="566ce-251">Из объекта `Identity` удалены нерекомендуемые свойства: `EncryptionState`, `EncryptionProvisioningState`, `EncryptionConfig`, `FirewallState`, `FirewallRules`, `VirtualNetworkRules`, `TrustedIdProviderState`, `TrustedIdProviders`, `DefaultGroup`, `NewTier`, `CurrentTier`, `FirewallAllowAzureIps`, `PSDataLakeStoreAccountBasic`.</span><span class="sxs-lookup"><span data-stu-id="566ce-251">Removed deprecated properties `Identity`, `EncryptionState`, `EncryptionProvisioningState`, `EncryptionConfig`, `FirewallState`, `FirewallRules`, `VirtualNetworkRules`, `TrustedIdProviderState`, `TrustedIdProviders`, `DefaultGroup`, `NewTier`, `CurrentTier`, `FirewallAllowAzureIps` from `PSDataLakeStoreAccountBasic` object.</span></span>  <span data-ttu-id="566ce-252">Любой сценарий, который использует `PSDatalakeStoreAccount`, возвращенный из `Get-AzDataLakeStoreAccount`, не должен ссылаться на эти свойства.</span><span class="sxs-lookup"><span data-stu-id="566ce-252">Any script that uses the `PSDatalakeStoreAccount` returned from `Get-AzDataLakeStoreAccount` should not reference these properties.</span></span>

### <a name="azkeyvault-previously-azurermkeyvault"></a><span data-ttu-id="566ce-253">Az.KeyVault (ранее AzureRM.KeyVault)</span><span class="sxs-lookup"><span data-stu-id="566ce-253">Az.KeyVault (previously AzureRM.KeyVault)</span></span>

- <span data-ttu-id="566ce-254">Свойство `PurgeDisabled` удалено из объектов `PSKeyVaultKeyAttributes`, `PSKeyVaultKeyIdentityItem` и `PSKeyVaultSecretAttributes`. Скрипты больше не должны ссылаться на свойство ```PurgeDisabled``` для принятия решений об обработке.</span><span class="sxs-lookup"><span data-stu-id="566ce-254">The `PurgeDisabled` property was removed from the `PSKeyVaultKeyAttributes`, `PSKeyVaultKeyIdentityItem`, and `PSKeyVaultSecretAttributes` objects Scripts should no longer reference the ```PurgeDisabled``` property to make processing decisions.</span></span>

### <a name="azmedia-previously-azurermmedia"></a><span data-ttu-id="566ce-255">Az.Media (ранее AzureRM.Media)</span><span class="sxs-lookup"><span data-stu-id="566ce-255">Az.Media (previously AzureRM.Media)</span></span>

- <span data-ttu-id="566ce-256">Удалите нерекомендуемый псевдоним свойства `Tags` из командлета `New-AzMediaService`. Сценарии, которые используют</span><span class="sxs-lookup"><span data-stu-id="566ce-256">Remove deprecated `Tags` property alias from `New-AzMediaService` cmdlet Scripts using</span></span>
  ```azurepowershell-interactive
  New-AzureRMMediaService -Tags @{TagName="TagValue"}
  ```

  <span data-ttu-id="566ce-257">следует изменить на</span><span class="sxs-lookup"><span data-stu-id="566ce-257">Should be changed to</span></span>
  ```azurepowershell-interactive
  New-AzMediaService -Tag @{TagName="TagValue"}
  ```

### <a name="azmonitor-previously-azurerminsights"></a><span data-ttu-id="566ce-258">Az.Monitor (ранее AzureRM.Insights)</span><span class="sxs-lookup"><span data-stu-id="566ce-258">Az.Monitor (previously AzureRM.Insights)</span></span>

- <span data-ttu-id="566ce-259">Множественные имена `Categories` и `Timegrains` параметра удалены в пользу единичных имен параметров из командлета `Set-AzDiagnosticSetting`. Сценарии, которые используют</span><span class="sxs-lookup"><span data-stu-id="566ce-259">Removed plural names `Categories` and `Timegrains` parameter in favor of singular parameter names from `Set-AzDiagnosticSetting` cmdlet Scripts using</span></span>
  ```azurepowershell-interactive
  Set-AzureRmDiagnosticSetting -Timegrains PT1M -Categories Category1, Category2
  ```

  <span data-ttu-id="566ce-260">следует изменить на</span><span class="sxs-lookup"><span data-stu-id="566ce-260">Should be changed to</span></span>
  ```azurepowershell-interactive
  Set-AzDiagnosticSetting -Timegrain PT1M -Category Category1, Category2
  ```

### <a name="aznetwork-previously-azurermnetwork"></a><span data-ttu-id="566ce-261">Az.Network (ранее AzureRM.Network)</span><span class="sxs-lookup"><span data-stu-id="566ce-261">Az.Network (previously AzureRM.Network)</span></span>

- <span data-ttu-id="566ce-262">Из командлета `ResourceId` удален нерекомендуемый параметр `Get-AzServiceEndpointPolicyDefinition`</span><span class="sxs-lookup"><span data-stu-id="566ce-262">Removed deprecated `ResourceId` parameter from `Get-AzServiceEndpointPolicyDefinition` cmdlet</span></span>
- <span data-ttu-id="566ce-263">Из объекта `EnableVmProtection` удалено нерекомендуемое свойство `PSVirtualNetwork`</span><span class="sxs-lookup"><span data-stu-id="566ce-263">Removed deprecated `EnableVmProtection` property from `PSVirtualNetwork` object</span></span>
- <span data-ttu-id="566ce-264">Нерекомендуемый командлет `Set-AzVirtualNetworkGatewayVpnClientConfig` удален</span><span class="sxs-lookup"><span data-stu-id="566ce-264">Removed deprecated `Set-AzVirtualNetworkGatewayVpnClientConfig` cmdlet</span></span>

<span data-ttu-id="566ce-265">Скрипты больше не должны принимать решения об обработке на основе значений этих полей.</span><span class="sxs-lookup"><span data-stu-id="566ce-265">Scripts should no longer make processing decisions based on the values fo these fields.</span></span>

### <a name="azoperationalinsights-previously-azurermoperationalinsights"></a><span data-ttu-id="566ce-266">Az.OperationalInsights (ранее AzureRM.OperationalInsights)</span><span class="sxs-lookup"><span data-stu-id="566ce-266">Az.OperationalInsights (previously AzureRM.OperationalInsights)</span></span>

- <span data-ttu-id="566ce-267">Набор параметров по умолчанию для `Get-AzOperationalInsightsDataSource` удален и заменен на `ByWorkspaceNameByKind`.</span><span class="sxs-lookup"><span data-stu-id="566ce-267">Default parameter set for `Get-AzOperationalInsightsDataSource` is removed, and `ByWorkspaceNameByKind` has become the default parameter set</span></span>

  <span data-ttu-id="566ce-268">Сценарии, в которых перечислены источники данных, использующие</span><span class="sxs-lookup"><span data-stu-id="566ce-268">Scripts that listed data sources using</span></span>
  ```azurepowershell-interactive
  Get-AzureRmOperationalInsightsDataSource
  ```

  <span data-ttu-id="566ce-269">следует изменить, чтобы указать вид</span><span class="sxs-lookup"><span data-stu-id="566ce-269">Should be changed to specify a Kind</span></span>
  ```azurepowershell-interactive
  Get-AzOperationalInsightsDataSource -Kind AzureActivityLog
  ```

### <a name="azrecoveryservices-previously-azurermrecoveryservices-azurermrecoveryservicesbackup-and-azurermrecoveryservicessiterecovery"></a><span data-ttu-id="566ce-270">Az.RecoveryServices (ранее AzureRM.RecoveryServices, AzureRM.RecoveryServices.Backup и AzureRM.RecoveryServices.SiteRecovery)</span><span class="sxs-lookup"><span data-stu-id="566ce-270">Az.RecoveryServices (previously AzureRM.RecoveryServices, AzureRM.RecoveryServices.Backup, and AzureRM.RecoveryServices.SiteRecovery)</span></span>

- <span data-ttu-id="566ce-271">Из командлета `Encryption` удален параметр `New/Set-AzRecoveryServicesAsrPolicy`.</span><span class="sxs-lookup"><span data-stu-id="566ce-271">Removed `Encryption` parameter from `New/Set-AzRecoveryServicesAsrPolicy` cmdlet</span></span>
- <span data-ttu-id="566ce-272">Параметр `TargetStorageAccountName` теперь является обязательным для восстановления управляемого диска в командлете `Restore-AzRecoveryServicesBackupItem`.</span><span class="sxs-lookup"><span data-stu-id="566ce-272">`TargetStorageAccountName` parameter is now mandatory for managed disk restores in `Restore-AzRecoveryServicesBackupItem` cmdlet</span></span>
- <span data-ttu-id="566ce-273">В командлете `StorageAccountName` удалены параметры `StorageAccountResourceGroupName` и `Restore-AzRecoveryServicesBackupItem`.</span><span class="sxs-lookup"><span data-stu-id="566ce-273">Removed `StorageAccountName` and `StorageAccountResourceGroupName` parameters in `Restore-AzRecoveryServicesBackupItem` cmdlet</span></span>
- <span data-ttu-id="566ce-274">В командлете `Name` удален параметр `Get-AzRecoveryServicesBackupContainer`.</span><span class="sxs-lookup"><span data-stu-id="566ce-274">Removed `Name`parameter in `Get-AzRecoveryServicesBackupContainer` cmdlet</span></span>

### <a name="azresources-previously-azurermresources"></a><span data-ttu-id="566ce-275">Az.Resources (ранее AzureRM.Resources)</span><span class="sxs-lookup"><span data-stu-id="566ce-275">Az.Resources (previously AzureRM.Resources)</span></span>

- <span data-ttu-id="566ce-276">Из командлета `Sku` удален параметр `New/Set-AzPolicyAssignment`.</span><span class="sxs-lookup"><span data-stu-id="566ce-276">Removed `Sku` parameter from `New/Set-AzPolicyAssignment` cmdlet</span></span>
- <span data-ttu-id="566ce-277">Параметр `Password` удален из командлетов `New-AzADServicePrincipal` и `New-AzADSpCredential`. Пароли генерируются автоматически. Сценарии, которые предоставили пароль:</span><span class="sxs-lookup"><span data-stu-id="566ce-277">Removed `Password` parameter from `New-AzADServicePrincipal` and `New-AzADSpCredential` cmdlet Passwords are automatically generated, scripts that provided the password:</span></span>

  ```azurepowershell-interactive
  New-AzAdSpCredential -ObjectId 1f99cf81-0146-4f4e-beae-2007d0668476 -Password $secPassword
  ```

  <span data-ttu-id="566ce-278">Следует изменить, чтобы получить пароль из выходных данных.</span><span class="sxs-lookup"><span data-stu-id="566ce-278">Should be changed to retrieve the password from the output:</span></span>

  ```azurepowershell-interactive
  $credential = New-AzAdSpCredential -ObjectId 1f99cf81-0146-4f4e-beae-2007d0668476
  $secPassword = $credential.Secret
  ```

### <a name="azservicefabric-previously-azurermservicefabric"></a><span data-ttu-id="566ce-279">Az.ServiceFabric (ранее AzureRM.ServiceFabric)</span><span class="sxs-lookup"><span data-stu-id="566ce-279">Az.ServiceFabric (previously AzureRM.ServiceFabric)</span></span>

- <span data-ttu-id="566ce-280">Следующие типы возвращаемого значения командлета были изменены.</span><span class="sxs-lookup"><span data-stu-id="566ce-280">The following cmdlet return types have been changed:</span></span>
  - <span data-ttu-id="566ce-281">Свойство `ServiceTypeHealthPolicies` типа `ApplicationHealthPolicy` удалено.</span><span class="sxs-lookup"><span data-stu-id="566ce-281">The property `ServiceTypeHealthPolicies` of type `ApplicationHealthPolicy` has been removed.</span></span>
  - <span data-ttu-id="566ce-282">Свойство `ApplicationHealthPolicies` типа `ClusterUpgradeDeltaHealthPolicy` удалено.</span><span class="sxs-lookup"><span data-stu-id="566ce-282">The property `ApplicationHealthPolicies` of type `ClusterUpgradeDeltaHealthPolicy` has been removed.</span></span>
  - <span data-ttu-id="566ce-283">Свойство `OverrideUserUpgradePolicy` типа `ClusterUpgradePolicy` удалено.</span><span class="sxs-lookup"><span data-stu-id="566ce-283">The property `OverrideUserUpgradePolicy` of type `ClusterUpgradePolicy` has been removed.</span></span>
  - <span data-ttu-id="566ce-284">Эти изменения влияют на следующие командлеты:</span><span class="sxs-lookup"><span data-stu-id="566ce-284">These changes affect the following cmdlets:</span></span>
    - <span data-ttu-id="566ce-285">Add-AzServiceFabricClientCertificate;</span><span class="sxs-lookup"><span data-stu-id="566ce-285">Add-AzServiceFabricClientCertificate</span></span>
    - <span data-ttu-id="566ce-286">Add-AzServiceFabricClusterCertificate;</span><span class="sxs-lookup"><span data-stu-id="566ce-286">Add-AzServiceFabricClusterCertificate</span></span>
    - <span data-ttu-id="566ce-287">Add-AzServiceFabricNode;</span><span class="sxs-lookup"><span data-stu-id="566ce-287">Add-AzServiceFabricNode</span></span>
    - <span data-ttu-id="566ce-288">Add-AzServiceFabricNodeType;</span><span class="sxs-lookup"><span data-stu-id="566ce-288">Add-AzServiceFabricNodeType</span></span>
    - <span data-ttu-id="566ce-289">Get-AzServiceFabricCluster;</span><span class="sxs-lookup"><span data-stu-id="566ce-289">Get-AzServiceFabricCluster</span></span>
    - <span data-ttu-id="566ce-290">Remove-AzServiceFabricClientCertificate;</span><span class="sxs-lookup"><span data-stu-id="566ce-290">Remove-AzServiceFabricClientCertificate</span></span>
    - <span data-ttu-id="566ce-291">Remove-AzServiceFabricClusterCertificate;</span><span class="sxs-lookup"><span data-stu-id="566ce-291">Remove-AzServiceFabricClusterCertificate</span></span>
    - <span data-ttu-id="566ce-292">Remove-AzServiceFabricNode;</span><span class="sxs-lookup"><span data-stu-id="566ce-292">Remove-AzServiceFabricNode</span></span>
    - <span data-ttu-id="566ce-293">Remove-AzServiceFabricNodeType;</span><span class="sxs-lookup"><span data-stu-id="566ce-293">Remove-AzServiceFabricNodeType</span></span>
    - <span data-ttu-id="566ce-294">Remove-AzServiceFabricSetting;</span><span class="sxs-lookup"><span data-stu-id="566ce-294">Remove-AzServiceFabricSetting</span></span>
    - <span data-ttu-id="566ce-295">Set-AzServiceFabricSetting;</span><span class="sxs-lookup"><span data-stu-id="566ce-295">Set-AzServiceFabricSetting</span></span>
    - <span data-ttu-id="566ce-296">Set-AzServiceFabricUpgradeType;</span><span class="sxs-lookup"><span data-stu-id="566ce-296">Set-AzServiceFabricUpgradeType</span></span>
    - <span data-ttu-id="566ce-297">Update-AzServiceFabricDurability;</span><span class="sxs-lookup"><span data-stu-id="566ce-297">Update-AzServiceFabricDurability</span></span>
    - <span data-ttu-id="566ce-298">Update-AzServiceFabricReliability.</span><span class="sxs-lookup"><span data-stu-id="566ce-298">Update-AzServiceFabricReliability</span></span>

### <a name="azsql-previously-azurermsql"></a><span data-ttu-id="566ce-299">Az.Sql (ранее AzureRM.Sql)</span><span class="sxs-lookup"><span data-stu-id="566ce-299">Az.Sql (previously AzureRM.Sql)</span></span>

- <span data-ttu-id="566ce-300">Из командлета `State` удалены параметры `ResourceId` и `Set-AzSqlDatabaseBackupLongTermRetentionPolicy`.</span><span class="sxs-lookup"><span data-stu-id="566ce-300">Removed `State` and `ResourceId` parameters from `Set-AzSqlDatabaseBackupLongTermRetentionPolicy` cmdlet</span></span>
- <span data-ttu-id="566ce-301">Удалены следующие нерекомендуемые командлеты: `Get/Set-AzSqlServerBackupLongTermRetentionVault`, `Get/Start/Stop-AzSqlServerUpgrade`, `Get/Set-AzSqlDatabaseAuditingPolicy`, `Get/Set-AzSqlServerAuditingPolicy`, `Remove-AzSqlDatabaseAuditing`, `Remove-AzSqlServerAuditing`.</span><span class="sxs-lookup"><span data-stu-id="566ce-301">Removed deprecated cmdlets: `Get/Set-AzSqlServerBackupLongTermRetentionVault`, `Get/Start/Stop-AzSqlServerUpgrade`, `Get/Set-AzSqlDatabaseAuditingPolicy`, `Get/Set-AzSqlServerAuditingPolicy`, `Remove-AzSqlDatabaseAuditing`, `Remove-AzSqlServerAuditing`</span></span>
- <span data-ttu-id="566ce-302">Из командлета `Current` удален нерекомендуемый параметр `Get-AzSqlDatabaseBackupLongTermRetentionPolicy`</span><span class="sxs-lookup"><span data-stu-id="566ce-302">Removed deprecated parameter `Current` from `Get-AzSqlDatabaseBackupLongTermRetentionPolicy` cmdlet</span></span>
- <span data-ttu-id="566ce-303">Из командлета `DatabaseName` удален нерекомендуемый параметр `Get-AzSqlServerServiceObjective`</span><span class="sxs-lookup"><span data-stu-id="566ce-303">Removed deprecated parameter `DatabaseName` from `Get-AzSqlServerServiceObjective` cmdlet</span></span>
- <span data-ttu-id="566ce-304">Из командлета `PrivilegedLogin` удален нерекомендуемый параметр `Set-AzSqlDatabaseDataMaskingPolicy`</span><span class="sxs-lookup"><span data-stu-id="566ce-304">Removed deprecated parameter `PrivilegedLogin` from `Set-AzSqlDatabaseDataMaskingPolicy` cmdlet</span></span>

### <a name="azstorage-previously-azurestorage-and-azurermstorage"></a><span data-ttu-id="566ce-305">Az.Storage (ранее Azure.Storage и AzureRM.Storage)</span><span class="sxs-lookup"><span data-stu-id="566ce-305">Az.Storage (previously Azure.Storage and AzureRM.Storage)</span></span>

- <span data-ttu-id="566ce-306">Для поддержки создания контекста хранения Oauth только с именем учетной записи хранения набор параметров по умолчанию был изменен на `OAuthParameterSet`.</span><span class="sxs-lookup"><span data-stu-id="566ce-306">To support creating an Oauth storage context with only the storage account name, the default parameter set has been changed to `OAuthParameterSet`</span></span>
  - <span data-ttu-id="566ce-307">Пример: `$ctx = New-AzureStorageContext -StorageAccountName $accountName`</span><span class="sxs-lookup"><span data-stu-id="566ce-307">Example: `$ctx = New-AzureStorageContext -StorageAccountName $accountName`</span></span>
- <span data-ttu-id="566ce-308">Параметр `Location` стал обязательным в командлете `Get-AzStorageUsage`</span><span class="sxs-lookup"><span data-stu-id="566ce-308">The `Location` parameter has become mandatory in the `Get-AzStorageUsage` cmdlet</span></span>
- <span data-ttu-id="566ce-309">Методы API службы хранилища теперь используют асинхронную модель на основе задач (TAP) вместо синхронных вызовов API.</span><span class="sxs-lookup"><span data-stu-id="566ce-309">The Storage API methods now use the Task-based Asynchronous Pattern (TAP), instead of synchronous API calls.</span></span> <span data-ttu-id="566ce-310">В приведенных ниже примерах показаны новые асинхронные команды.</span><span class="sxs-lookup"><span data-stu-id="566ce-310">The following examples demonstrate the new asynchronous commands:</span></span>

#### <a name="blob-snapshot"></a><span data-ttu-id="566ce-311">Моментальный снимок большого двоичного объекта</span><span class="sxs-lookup"><span data-stu-id="566ce-311">Blob Snapshot</span></span>

<span data-ttu-id="566ce-312">AzureRM:</span><span class="sxs-lookup"><span data-stu-id="566ce-312">AzureRM:</span></span>

```azurepowershell-interactive
$b = Get-AzureStorageBlob -Container $containerName -Blob $blobName -Context $ctx
$b.ICloudBlob.Snapshot()
```

<span data-ttu-id="566ce-313">Az:</span><span class="sxs-lookup"><span data-stu-id="566ce-313">Az:</span></span>

```azurepowershell-interactive
$b = Get-AzureStorageBlob -Container $containerName -Blob $blobName -Context $ctx
$task = $b.ICloudBlob.SnapshotAsync()
$task.Wait()
$snapshot = $task.Result
```

#### <a name="share-snapshot"></a><span data-ttu-id="566ce-314">Общий доступ к снимку</span><span class="sxs-lookup"><span data-stu-id="566ce-314">Share Snapshot</span></span>

<span data-ttu-id="566ce-315">AzureRM:</span><span class="sxs-lookup"><span data-stu-id="566ce-315">AzureRM:</span></span>

```azurepowershell-interactive
$Share = Get-AzureStorageShare -Name $containerName -Context $ctx
$snapshot = $Share.Snapshot()
```

<span data-ttu-id="566ce-316">Az:</span><span class="sxs-lookup"><span data-stu-id="566ce-316">Az:</span></span>

```azurepowershell-interactive
$Share = Get-AzureStorageShare -Name $containerName -Context $ctx
$task = $Share.SnapshotAsync()
$task.Wait()
$snapshot = $task.Result
```

#### <a name="undelete-soft-deleted-blob"></a><span data-ttu-id="566ce-317">Отмена удаления обратимо удаленных больших двоичных объектов</span><span class="sxs-lookup"><span data-stu-id="566ce-317">Undelete soft-deleted blob</span></span>

<span data-ttu-id="566ce-318">AzureRM:</span><span class="sxs-lookup"><span data-stu-id="566ce-318">AzureRM:</span></span>

```azurepowershell-interactive
$b = Get-AzureStorageBlob -Container $containerName -Blob $blobName -IncludeDeleted -Context $ctx
$b.ICloudBlob.Undelete()
```

<span data-ttu-id="566ce-319">Az:</span><span class="sxs-lookup"><span data-stu-id="566ce-319">Az:</span></span>

```azurepowershell-interactive
$b = Get-AzureStorageBlob -Container $containerName -Blob $blobName -IncludeDeleted -Context $ctx
$task = $b.ICloudBlob.UndeleteAsync()
$task.Wait()
```

#### <a name="set-blob-tier"></a><span data-ttu-id="566ce-320">Установка уровня большого двоичного объекта</span><span class="sxs-lookup"><span data-stu-id="566ce-320">Set Blob Tier</span></span>

<span data-ttu-id="566ce-321">AzureRM:</span><span class="sxs-lookup"><span data-stu-id="566ce-321">AzureRM:</span></span>

```azurepowershell-interactive
$blockBlob = Get-AzureStorageBlob -Container $containerName -Blob $blockBlobName -Context $ctx
$blockBlob.ICloudBlob.SetStandardBlobTier("hot")

$pageBlob = Get-AzureStorageBlob -Container $containerName -Blob $pageBlobName -Context $ctx
$pageBlob.ICloudBlob.SetPremiumBlobTier("P4")
```

<span data-ttu-id="566ce-322">Az:</span><span class="sxs-lookup"><span data-stu-id="566ce-322">Az:</span></span>

```azurepowershell-interactive
$blockBlob = Get-AzureStorageBlob -Container $containerName -Blob $blockBlobName -Context $ctx
$task = $blockBlob.ICloudBlob.SetStandardBlobTierAsync("hot")
$task.Wait()

$pageBlob = Get-AzureStorageBlob -Container $containerName -Blob $pageBlobName -Context $ctx
$task = $pageBlob.ICloudBlob.SetPremiumBlobTierAsync("P4")
$task.Wait()
```

### <a name="azwebsites-previously-azurermwebsites"></a><span data-ttu-id="566ce-323">Az.Websites (ранее AzureRM.Websites)</span><span class="sxs-lookup"><span data-stu-id="566ce-323">Az.Websites (previously AzureRM.Websites)</span></span>

- <span data-ttu-id="566ce-324">Из объектов `PSAppServicePlan`, `PSCertificate`, `PSCloningInfo` и `PSSite` удалены нерекомендуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="566ce-324">Removed deprecated properties from the `PSAppServicePlan`, `PSCertificate`, `PSCloningInfo`, and `PSSite` objects</span></span>
